<template>
  <div id="app">
    <SalesComponent></SalesComponent>
  </div>
</template>

<script>
import SalesComponent from './components/SalesComponent.vue'

export default {
  components: {
    SalesComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans - serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>