<template>
    <header>
        <h1>{{ title }}</h1>
        <Button @toggle-add-task="$emit('toggle-add-task')" @click="logData()" text="Add task" color="black"/>
    </header>
</template>

<script>
import Button from "./Button.vue";
    export default {
        name: 'Header',
        props: {
            title: {
                type: String,
                }
        },
        components: {
            Button
        },
        methods: {
            logData() {
                console.log('Hello, dumbass!');
            }
        }
    }
</script>

<style scoped>
    header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    }    
</style>