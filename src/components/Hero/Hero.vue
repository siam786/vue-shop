<script setup>
import { RouterLink } from "vue-router";
</script>
<template>
  <div class="bg-sky-700 h-[550px] flex justify-center">
    <div class="container flex items-center justify-between mx-auto">
      <div class="w-1/2 space-y-3">
        
        <h1 class="text-white text-5xl font-[800] font-mon">
         awesome shop for every day
        </h1>
        <p class="text-sm text-white font-[400] font-mon">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quas, eligendi obcaecati accusamus autem nisi laborum cum assumenda repellat at neque ratione sit, odio nesciunt necessitatibus cumque eos cupiditate fugit aut?
        </p>
        <button>
          <RouterLink
            to="/shop"
            class="px-4 py-2 text-white rounded bg-primary"
          >
            Shop Now
          </RouterLink>
        </button>
      </div>
      <div>
        <img class="w-80 " src="../../assets/images/pngimg.com - phone_hand_PNG21.png" alt="" />
      </div>
    </div>
  </div>
</template>

<style scoped></style>
