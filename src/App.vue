<template>
  <div id="app">
    <KeyEventTest msg="Key Event TEST"/>
  </div>
</template>

<script>
import KeyEventTest from './components/KeyEventTest.vue'

export default {
  name: 'App',
  components: {
    KeyEventTest
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
