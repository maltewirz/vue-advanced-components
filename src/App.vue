<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <button @click="selectedComponent = 'Quote'">Quote</button>
                <button @click="selectedComponent = 'Author'">Author</button>
                <button @click="selectedComponent = 'New'">New</button>

                <component :is="selectedComponent">
                    <p>Default Content</p>
                </component>
                <!-- <Quote>
                    <h2 slot="title"> {{ quoteTitle }} </h2>
                    <p slot="content">A wonderful quote!</p>
                </Quote> -->
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';
    import Author from './components/Author.vue';
    import New from './components/New.vue';

    export default {
        data: function() {
            return {
                quoteTitle: 'The quote',
                selectedComponent: 'Quote'
            }
        },
        components: {
            Quote,
            Author,
            New,
        }
        
    }
</script>

<style scoped>


</style>
