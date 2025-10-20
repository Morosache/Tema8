<script setup>
import { ref } from 'vue';
  const colors = ['bg-blue500', 'bg-green-300', 'bg-pink-200', 'bg-gray-400', 'bg-purple-200', 'bg-yellow-500']
  const colorClass = ref('bg-red-500');

  const changeColor = () => {
    const randomColor = Math.floor(Math.random() * colors.length);
    colorClass.value = colors[randomColor];
  }
</script>

<template>
  <div class="flex justify-center items-center flex-col gap-5 h-screen w-screen">
    <button @click="changeColor" class= "text-[15px] font-semibold px-[40px] py-[8px] bg-gray-200">Genereaza culoare</button>
    <div :class="['w-[300px]', 'h-[300px]', colorClass, 'border-[2px]']"></div>
  </div>
</template>

<style scoped></style>
