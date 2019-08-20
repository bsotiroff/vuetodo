<template>
  <div id="app">
    <DinoCard/>
  </div>
</template>

<script>
import DinoCard from './components/DinoCard.vue'

export default {
  name: 'app',
  components: {

    DinoCard,
  }
}
</script>

<style>
#app {
  font-family: 'Roboto', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
