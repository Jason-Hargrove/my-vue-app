<script setup>
import { ref } from "vue";

const useChangeWithDelay = (state, newVal, delay) => {
  setTimeout(() => {
    state.value = newVal;
  }, delay);
};

const product = ref("Socks");

useChangeWithDelay(product, "New Socks", 1000);
</script>

<template>
  <div class="nav-bar"></div>
  <div class="product-display">
    <div class="product-container">
      <div class="product-image"><!-- image goes here --></div>
      <div class="product-info">
        <h1>{{ product }}</h1>
      </div>
    </div>
  </div>
</template>
