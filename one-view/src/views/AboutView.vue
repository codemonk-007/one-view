<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h2 class="continue" @click="routeToSecondPage">{{ tag }}</h2>
  </div>
</template>
<script>
export default {
  data() {
    return {
      tag: "Continue from here ",
    };
  },
  methods: {
    routeToSecondPage() {
      this.$router.push({ name: "home" });
    },
  },
};
</script>
<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
  }
  .continue:hover {
    color: bisque;
  }
}
</style>
