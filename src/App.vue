<template>
  <div id="app">
    <todo></todo>
  </div>
</template>

<script>
import { mapGetters } from 'vuex';
import Todo from './components/todo.vue'

export default {
  name: 'app',
  components: {
    Todo
  },
  data() {
    return {
      todo_message: ''
    }
  },
  methods: {
    addTodo() {
      this.$store.dispatch('ADD_TODO', this.todo_message)
      this.todo_message = '';
    },
    deleteTodo(index) {
      this.$store.dispatch('REMOVE_TODO', index);
    }
  },
  computed: {
    ...mapGetters(['todos'])
  }
}
</script>

<style scoped>
.del-btn {
  color: red;
  margin-left:30px;
  cursor: pointer;
}
table {
  border-collapse: collapse;
  margin-top: 20px;
}
table, th, td {
  border: 1px solid black;
}
td {
  padding: 5px;
}
#app {
  text-align: center;
}
</style>
