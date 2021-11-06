<template>
  <h1>Home Page</h1>
</template>

<script>
export default {
  // with keep-alive the component does not get unmoanted
  unmounted() {
    console.log("Home component unmounted!");
  },
  activated() {
    console.log("Home component activated");
  },
  deactivated() {
    console.log("Home component deactivated");
  },
};
</script>

<style></style>
