<template>
    <div>
        <h3>New Quote</h3>
        <button @click="counter++"></button>
        {{counter}}
    </div>
</template>

<script>
    export default {
        data: function(){
            return {
                counter: 0
            }
        },
        deactivated() {
            console.log("Deactivated");
        },
        activated() {
            console.log('Activated');
        }
    }
</script>

<style scoped>

</style>