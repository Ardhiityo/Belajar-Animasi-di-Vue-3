<template>
  <div>
    <transition name="fade">
      <div v-if="showContent">
        <h1>Hello World</h1>
      </div>
    </transition>
    <button @click="showContent = !showContent">Click me!</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const showContent = ref(true);
</script>

<style scoped>
.fade-enter-from {
  opacity: 0;
}
.fade-enter-to {
  opacity: 1;
}
.fade-enter-active {
  transition: all 1s ease;
}
</style>