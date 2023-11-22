<template>
  <div class="container">
    <headerUser />
    <cardUser />
  </div>
</template>

<script>
import cardUser from "./components/cardUser.vue";
import headerUser from "./components/headerUser.vue";
export default {
  name: "App",
  components: {
    cardUser,
    headerUser,
  },
};
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
