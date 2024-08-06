
<template>
<h1>Vue 3 Todo App</h1>
<form action="#" @submit.prevent="addNewTodo">
  <label for="#" >New Todo</label>
  <input v-model="newTodo" type="text" name="newTodo">
  <button>Add New Todo</button>
</form>
<h2>{{newTodo}}</h2>
</template>

  <script>
  import { ref } from "vue";

  export default {
    setup() {
      const newTodo = ref('')

      function addNewTodo() {
        console.log("Form was submitted");
    }
    return {newTodo, addNewTodo}
      
    }
  }

  </script>

<style scoped>
body {
  font-family: sans-serif;
  padding-top: 1em;
  padding-bottom: 1em;
  font-size: 2em;
  width: 100%;
  margin: 0 auto;
}
</style>
