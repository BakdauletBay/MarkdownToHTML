<template>
  <div id="app">
    <TestWindow />
  </div>
</template>

<script>
import TestWindow from "./components/TestWindow.vue";

export default {
  name: "App",
  components: {
    TestWindow,
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