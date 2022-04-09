<script setup>
import { defineProps } from "vue";

const { text } = defineProps({
    text: String,
});
</script>

<template>
    <ruby class="kaiti">
        <slot />
        <rp>(</rp>
        <rt class="roman">{{ text }}</rt>
        <rp>)</rp>
    </ruby>
</template>

<style scoped>
.kaiti {
    font-family: "Ma Shan Zheng";
}
.roman {
    /* font-family: "Merriweather"; */
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
        Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    font-weight: normal;
}
</style>
