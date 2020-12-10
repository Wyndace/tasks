<template>
    <ul>
        <li v-for="(todo, index) in todos" v-on:click="deleteTodo(index)" v-bind:key="index">{{ todo }}</li>
    </ul>
</template>

<script>
export default {
    props: ['todos'],
    methods: {
        deleteTodo(index){
            this.$emit('delete-todo', index);
        }
    }
}
</script>

<style>
ul{
    display: flex;
    flex-direction: column;
    width: 99%;
    padding: 0;
}
 li {
     display: inline-block;
    max-height: 50px;
    min-width: 100px;
    padding: 5px;
    margin: 0 0 5px 0;
    background: rgb(235, 241, 240);
  }
  li::before {
    height:10px;
    width: 10px;
    content: "";
    border-radius: 25px;
    background: rgb(93, 226, 98);
    display: inline-block;
    margin: 0 15px 0px 0px;
  }
</style>