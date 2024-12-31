<script setup>
import { useRoute, useRouter } from "vue-router";

const router = useRouter();
const route = useRoute();
console.log('path', route.path);
console.log('name', route.name);


const redirectToUser = () => {
  router.push({ name: 'user' });
};
</script>

<template>
  <div class="about">
    <h1>This is an about page.</h1>
    <button @click="redirectToUser">Redirect About User</button>
    <!-- <RouterLink to="/about/user">Redirect About User</RouterLink> -->
    <router-view></router-view>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
