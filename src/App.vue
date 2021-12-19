<template>
  <Form @add="addTodo" />
  <List :allTodos="allTodos" />
</template>

<script>
import Form from './components/Form.vue'
import List from './components/List.vue'

export default {
  name: 'App',
  components: {
    Form,
    List
  },
  data: () => { 
    return {
      allTodos: []
    }
  },
  methods: {
    addTodo(title) {
      this.allTodos.push({id: this.allTodos.length + 1, title: title, done: false})
    }
  }
}
</script>