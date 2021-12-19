<template>
  <div>
    <input v-model="title" placeholder="TODO">
    <button @click="add">add</button>
  </div>
</template>

<script>
export default {
  name: 'Form',
  data() {
    return {
      title: '',
    }
  },
  methods: {
    add() {
      this.$emit('add', this.title)
      this.title = ''
    }
  }
}
</script>

<style scoped>
div {
    background-color: #ddeedd;
}
</style>