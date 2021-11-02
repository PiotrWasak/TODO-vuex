<template>
  <div id="app" class="container-fluid">
    <div class="row">
      <div class="col-md-6"><todo></todo></div>
      <div class="col-md-6"><todo></todo></div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import Todo from "./components/todo.vue";

export default {
  name: "app",
  components: {
    Todo,
  },
};
</script>

<style scoped>
#app {
  margin-top: 10vh;
}
</style>
