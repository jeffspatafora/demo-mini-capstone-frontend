<script>
export default {
  data: function () {
    return {
      message: "Products Index",
      products: []
    };
  },
  created: function () { },
  methods: {},
};
</script>

<template>
  <div class="home">
    <h1>{{ products }}</h1>
    <h1>{{ message }}</h1>
  </div>
</template>

<style>
</style>