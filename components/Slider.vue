<template>
    <div class="relative overflow-hidden h-96 mt-12">
      <!-- Slider Container -->
      <div
        class="flex transition-transform ease-out duration-500"
        :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
      >
        <!-- Image Slides -->
        <div
          v-for="(image, index) in images"
          :key="index"
          class="flex-shrink-0 w-full h-96"
        >
          <img
            :src="image"
            alt="Slider Image"
            class="w-full h-full object-cover"
          />
        </div>
      </div>
  
      <!-- Controls -->
      <button
        @click="prev"
        class="absolute top-1/2 left-2 transform -translate-y-1/2 bg-gray-700 text-white p-1 rounded-full hover:bg-gray-600 z-10"
      >
        &lt;
      </button>
      <button
        @click="next"
        class="absolute top-1/2 right-2 transform -translate-y-1/2 bg-gray-700 text-white p-1 rounded-full hover:bg-gray-600 z-10"
      >
        &gt;
      </button>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const images = [
    '/assets/tiling-1.jpg',
    '/assets/tiling-3.jpg',
    '/assets/tiling-2.webp',
  ]
  const currentIndex = ref(0)
  
  function next() {
    currentIndex.value = (currentIndex.value + 1) % images.length
  }
  
  function prev() {
    currentIndex.value = (currentIndex.value - 1 + images.length) % images.length
  }
  </script>
  
  <style scoped></style>
  