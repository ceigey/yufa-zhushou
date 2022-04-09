<script setup>
import { ref } from "vue";

const count = ref(0);

const inc = () => count.value++;
const dec = () => count.value--;
</script>

<template>
  <div>
    <button @click="dec(count)">to {{ count - 1 }}</button>
    <button @click="inc(count)">to {{ count + 1 }}</button>
    <p>Current count: {{ count }}</p>
  </div>
</template>

<style scoped>
button {
  min-width: 5em;
}
</style>
