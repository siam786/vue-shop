<script setup>
import { ref } from "vue";
import { authStore } from "../store/authStore";
import router from "../router";
const auth = authStore;
const email = ref("");
const password = ref("");
</script>
<template>
  <section class="bg-slate-100 h-screen flex items-center justify-center">
    <div class="bg-white px-6 max-w-lg w-full py-8 rounded">
      <h5 class="text-2xl text-center font-[700] text-red-700">
        Sign in to our platform
      </h5>
      <div class="my-6">
        <label
          for="email"
          class="block mb-2 text-sm font-medium text-gray-900"
          >Enter Your Email</label
        >
        <div class="relative">
          <div
            class="absolute inset-y-0 left-0 flex items-center pl-3.5 pointer-events-none"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-4 h-4 text-gray-500"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75"
              />
            </svg>
          </div>
          <input
            v-model="email"
            type="email"
            id="email"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
            placeholder="name@example.com"
          />
        </div>
      </div>
      <div class="my-6">
        <label
          for="password"
          class="block mb-2 text-sm font-medium text-gray-900"
          >Enter Your Password</label
        >
        <div class="relative">
          <div
            class="absolute inset-y-0 left-0 flex items-center pl-3.5 pointer-events-none"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-4 h-4 text-gray-500 dark:text-gray-400"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M16.5 10.5V6.75a4.5 4.5 0 10-9 0v3.75m-.75 11.25h10.5a2.25 2.25 0 002.25-2.25v-6.75a2.25 2.25 0 00-2.25-2.25H6.75a2.25 2.25 0 00-2.25 2.25v6.75a2.25 2.25 0 002.25 2.25z"
              />
            </svg>
          </div>
          <input
            v-model="password"
            type="password"
            id="password"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
            placeholder="********"
          />
        </div>
      </div>
      <button
        @click="auth.authenticate(email, password)"
        class="bg-primary text-white py-2 px-4 rounded w-full mt-3"
      >
        Login
      </button>
      <div class="text-sm font-medium text-gray-500 dark:text-gray-300 mt-3">
        Not registered?
        <RouterLink to="/register" class="text-blue-700 hover:underline"
          >Create account</RouterLink
        >
      </div>
    </div>
  </section>
</template>

<style scoped></style>
