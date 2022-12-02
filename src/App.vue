<script setup>
import { ref } from "vue";
import socksGreenImage from './assets/images/socks_green.jpeg'

const useChangeWithDelay = (state, newVal, delay) => {
  setTimeout(() => {
    state.value = newVal;
  }, delay);
};

const product = ref("Socks");
const image = ref(socksGreenImage)

useChangeWithDelay(product, "New Socks", 1000);
</script>

<template>
  <div class="nav-bar"></div>
  <div class="product-display">
    <div class="product-container">
      <div class="product-image">
        <img v-bind:src="image">
      </div>
      <div class="product-info">
        <h1>{{ product }}</h1>
        <p>In Stock</p>
        <p>Out of Stock</p>
      </div>
    </div>
  </div>
</template>
