<template>
  <div id="app">
    <img src="./assets/logo.png">
    <TodoMVC/>
  </div>
</template>

<script>
import TodoMVC from './components/TodoMVC'

export default {
  name: 'app',
  components: {
    TodoMVC
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
