<script setup>
import { RouterView } from "vue-router";
import VHeader from "./components/VHeader.vue";
</script>

<template>
  <VHeader />
  <RouterView />
  <VFooter />
</template>

<style scoped></style>
