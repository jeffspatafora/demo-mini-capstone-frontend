<script>
import axios from "axios";
export default {
  data: function () {
    return {
      message: "Products Index",
      products: []
    };
  },
  created: function () { },
  methods: {
    indexProducts: function () {
      console.log("in index");
      axios.get("/products.json").then(response => {
        this.products = response.data;
        console.log(response.data);
      })
    }
  },
};
</script>

<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <div v-for="product in products" v-bind:key="product.id">
      {{ product.name }}
      <!-- <img v-bind:src="product.images" v-bind:alt="product.name" /> -->
    </div>
    <button v-on:click="indexProducts()">index</button>
  </div>
</template>

<style>
</style>