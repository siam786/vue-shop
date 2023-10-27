<script setup>
import { RouterLink } from "vue-router";
</script>
<template>
  
  <div class="hero min-h-screen bg-base-200">
  <div class="hero-content flex-col lg:flex-row">
    <img src="../../assets/images/pngimg.com - phone_hand_PNG21.png" class="max-w-sm rounded-lg shadow-2xl" />
    <div>
      <h1 class="text-5xl font-bold">Hurry Up Limited Offer!</h1>
      <p class="py-6">The iPhone is a revolutionary smartphone known for its sleek design, powerful performance, and innovative features that enhance user experience</p>
      <button class="btn btn-primary"> <RouterLink
            to="/shop"
            
          >
            Shop Now
          </RouterLink></button>
    </div>
  </div>
</div>
</template>

<style scoped></style>
