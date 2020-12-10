<template>
  <div id="app">
    <TodoList v-bind:todos="todos" v-on:delete-todo="deleteTodo"/>
  </div>
</template>

<script>
import TodoList from './components/ToDoList';

export default {
  name: 'app',
  data(){
    return {
      todos: ['Зарядка', 'Завтрак', 'подписаться на vk.com/wynyard_memes', 'лайкнуть все мемы на vk.com/wynyard_memes']
    }
  },
  components: {
    TodoList
  },
  methods: {
    deleteTodo(index){
      this.todos.splice(index, 1);
    }
  }
}
</script>

<style>
 #app{
   width: 100vw;
   margin: 0;
 }
</style>