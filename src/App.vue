<template>
  <select v-model="componentName">
    <option value="Home">Home</option>
    <option value="About">About</option>
  </select>

  <!-- By default dynamic components lose all data on unmoant -->
  <!-- using keep-alive vue will save in memory the component and its data-->
  <keep-alive>
    <component :is="componentName"></component>
  </keep-alive>
</template>

<script>
import Home from "./components/Home.vue";
import About from "./components/About.vue";

export default {
  name: "App",
  components: {
    Home,
    About,
  },
  data() {
    return {
      componentName: "Home",
    };
  },
};
</script>
