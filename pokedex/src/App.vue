<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/pokemonlogo.png" class="logo">
    <Pokemon />
  </div>
</template>

<script>
import Pokemon from './components/Pokemon.vue'

export default {
  components: {
    Pokemon
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

.logo{
  height: 10vh;
}
</style>
