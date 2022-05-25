<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import TheWelcome from "./components/TheWelcome.vue";
import { ref } from "vue";

const showMenu = ref(false);

const toggleMenu = () => {
  console.log('test')
  showMenu.value = !showMenu.value;
};
</script>

<template>
  <body class="w-screen">
    <nav class="sm:bg-transparent w-screen z-50 fixed bg-black opacity-75">
      <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
        <div class="relative flex items-center justify-between h-16">
          <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
            <!-- Mobile menu button-->
            <button
              @click="toggleMenu"
              type="button"
              class="inline-flex items-center justify-center p-2 rounded-full text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
            >
              <span class="sr-only">Open main menu</span>
              <svg
                class="block h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="2"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M4 6h16M4 12h16M4 18h16"
                />
              </svg>
              <svg
                class="hidden h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="2"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M6 18L18 6M6 6l12 12"
                />
              </svg>
            </button>
          </div>
          <div
            class="mx-auto flex items-center justify-center sm:justify-center"
          >
            <div class="flex-shrink-0 flex items-center">
              <img class="h-8 w-auto" src="./assets/logo.svg" alt="Workflow" />
            </div>
            <div class="hidden sm:block sm:ml-6">
              <div class="flex space-x-6">
                <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
                <a
                  href="#"
                  class="text-white text-u py-2 text-sm font-medium border-b-2"
                  aria-current="page"
                  >Yachts</a
                >

                <a
                  href="#beyond2"
                  class="text-gray-300 hover:bg-gray-700 hover:text-white py-2 rounded-full text-sm font-medium"
                  >Travel Styles</a
                >

                <a
                  href="#"
                  class="text-gray-300 hover:bg-gray-700 hover:text-white py-2 rounded-full text-sm font-medium"
                  >Services</a
                >

                <a
                  href="#"
                  class="text-gray-300 hover:bg-gray-700 hover:text-white py-2 rounded-full text-sm font-medium"
                  >Our Vision</a
                >

                <a
                  href="#"
                  class="text-gray-300 hover:bg-gray-700 bg-gray-700 hover:text-white px-3 py-2 rounded-full text-sm font-medium"
                  >Enquire now</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Mobile menu, show/hide based on menu state. -->
      <div v-if="showMenu" class="sm:hidden" id="mobile-menu">
        <div class="px-2 pt-2 pb-3 space-y-1 bg-black opacity-75">
          <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
          <a
            href="#"
            class="text-white text-u px-3 py-2 block text-sm font-medium border-b-2"
            aria-current="page"
            >Yachts</a
          >

          <a
            href="#beyond2"
            class="text-gray-300 hover:bg-gray-700 block hover:text-white px-3 py-2 rounded-full text-sm font-medium"
            >Travel Styles</a
          >

          <a
            href="#"
            class="text-gray-300 hover:bg-gray-700 block hover:text-white px-3 py-2 rounded-full text-sm font-medium"
            >Services</a
          >

          <a
            href="#"
            class="text-gray-300 hover:bg-gray-700 block hover:text-white px-3 py-2 rounded-full text-sm font-medium"
            >Our Vision</a
          >

          <a
            href="#"
            class="text-gray-300 hover:bg-gray-700 block bg-gray-700 hover:text-white px-3 py-2 rounded-full text-sm font-medium"
            >Enquire now</a
          >
        </div>
      </div>
    </nav>

    <section
      id="beyond"
      class="flex items-center justify-center h-screen bg-[url('./src/assets/background.jpg')]"
    >
      <div class="flex flex-col justify-center items-center w-5/12 text-center">
        <h1 class="text-5xl text-neutral-700 my-5">
          Beyond the ordinary seas.
        </h1>
        <h4 class="text-2xl text-neutral-700">
          Delivering one of the finest yacht experience in the adriatic sea
        </h4>
      </div>
    </section>

    <section
      id="beyond2"
      class="flex items-center justify-center h-screen bg-[url('./src/assets/background.jpg')]"
    >
      <div class="flex flex-col justify-center items-center w-5/12 text-center">
        <h1 class="text-5xl text-neutral-700 my-5">
          Beyond the not so ordinary seas.
        </h1>
        <h4 class="text-2xl text-neutral-700">
          Delivering one of the finest yacht experience in the adriatic sea
        </h4>
      </div>
    </section>
  </body>
</template>

<style>
@import "./assets/base.css";

.background-image {
  background: url("./assets/background.jpg");
}
</style>
