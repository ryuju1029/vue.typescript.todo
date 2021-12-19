<template>
  <div>
    <ol>
      <template v-for="(todo, index) in todos" :key="todo.id">
         <li v-if="!todo.done">
           {{todo.title}}
           <button @click="done(index)">done</button>
         </li> 
      </template>    
    </ol>
  </div>   
</template>

<script>
export default {
  name: 'List',
  props: {
    allTodos: Array
  },
  data() {
    return {
      todos: this.allTodos,
    }
  },
  methods: {
    done(index) {
      this.todos[index].done = true
    }
  }
}
</script>

<style scoped>
div {
  background-color: #eeddee;
}
</style>