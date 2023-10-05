<script setup>
import { ref } from 'vue'

const bg = ref('text-yellow-500')
const color = ref('#FBBF24')
function addBackground() {
  bg.value = 'p-5 rounded bg-yellow-500 text-white duration-200 origin-left'
  color.value = '#ffffff'
}

function removeBackground() {
  bg.value = 'text-yellow-500'
  color.value = '#FBBF24'
}
</script>

<template>
  <div class="flex">
    <div class="w-1/6"></div>
    <div class="absolute right-80 top-12 flex space-x-4">
      <span class="bg-yellow-500 px-6 py-2"></span>
      <span class="bg-yellow-500 px-12 py-2"></span>
    </div>
    <div class="absolute text-9xl font-bold text-yellow-500 left-96 top-24">We Create</div>
    <div class="w-4/6 h-screen bg-gray-100 flex justify-center items-center px-32">
      <img src="./assets/photo.webp" alt="photo" class="w-full h-2/3 object-cover">
    </div>
    <div class="absolute text-6xl font-bold left-96 bottom-32 flex justify-center items-center space-x-8" :class="[bg]"
      @mouseover="addBackground()" @mouseleave="removeBackground()">
      <span>AWESOME THINGS</span>
      <svg width="90" height="90" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg">
        <path :fill="color" fill-rule="evenodd"
          d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8z" />
      </svg>
    </div>
    <div class="absolute left-80 bottom-12 flex space-x-4">
      <span class="bg-yellow-500 px-6 py-2"></span>
      <span class="bg-yellow-500 px-12 py-2"></span>
    </div>
    <div class="w-1/6"></div>
  </div>
</template>

<style scoped>

</style>
