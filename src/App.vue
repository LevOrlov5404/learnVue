<template>
  <div id="app">
    <ToDoList :todos="todos" @delete-todo="deleteToDo"/>
  </div>
</template>

<script>
import ToDoList from './components/ToDoList'

export default {
  name: 'App',
  data() {
    return {
      todos: ['Ремонт', 'Завтрак']
    }
  },
  components: {
    ToDoList
  },
  methods: {
    deleteToDo(index) {
      this.todos.splice(index, 1);
    }
  }
}
</script>

<style>

</style>
