<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>{{ data }}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      data: {}
    }
  },
  mounted() {
    const url = import.meta.env.VITE_PATH
    this.$http
      .get(url)
      .then((res) => (this.data = res.data.results[0]))
      .catch((e) => console.log(e))
  }
}
</script>
<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
