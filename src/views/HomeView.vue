<script setup>
import { ref } from "vue";
import TheWelcome from "../components/TheWelcome.vue";

const count = ref(10);
const handleIncrease = (value) => {
  count.value = count.value + value;
};
</script>

<template>
  <main>
    <TheWelcome :count="count" @handle-increase="handleIncrease" />
  </main>
</template>
