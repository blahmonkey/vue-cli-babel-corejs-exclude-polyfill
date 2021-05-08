<template>
  <div>
    <h1>Polyfill exclusion principle</h1>
    <h2>Status: {{ status }}</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  data() {
    return {
      status: "Loading",
    };
  },
  mounted() {
    const url = new URL("http://www.google.com/?data=unknown");
    this.status = `Loaded: ${url.toString()}`;
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
