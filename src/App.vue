<template>
  <div class="container">
    <!-- elemen yg berada di dlm transition hnya boleh memiliki 1, kecuali memiliki kondisi lain -->
    <transition name="fade"> 
      <h1 v-if="showContent">Hello World</h1>
      <h1 v-else>Good bye</h1>
    </transition>
    <button @click="showContent = !showContent">Click me!</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const showContent = ref(true);
</script>

<style scoped>
.container {
  position: relative;
}
h1 {
  position: absolute;
}
button {
  margin-top: 80px;
}
.fade-enter-from {
  opacity: 0;
}
.fade-enter-to {
  opacity: 1;
}
.fade-enter-active {
  transition: all 1s ease;
}
.fade-leave-from {
  opacity: 1;
}
.fade-leave-to {
  opacity: 0;
}
.fade-leave-active {
  transition: all 1s ease;
}
</style>