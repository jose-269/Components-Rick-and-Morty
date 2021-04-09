<template>
  <div id="app">
    <h1 class="mainTitle pt-5 mb-5">Rick And Morty</h1>
    <Personajes />
  </div>
</template>

<script>
import Personajes from "./components/Personajes.vue";

export default {
  name: "App",
  components: {
    Personajes,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  // margin-top: 60px;
}
body {
  margin: 0;
  background-image: url(https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png);
  background-position: center;
  background-repeat: repeat-y;
  background-size: cover;
  height: 100vh;
  h1 {
    margin: 0;
  }
}
</style>
