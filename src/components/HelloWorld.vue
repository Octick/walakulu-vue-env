<script setup lang="ts">
const variable = import.meta.env.VITE_APP_NAME as string;
const isVariable = variable !== undefined && variable.trim() !== "";
</script>

<template>
  <div class="container">
    <p>vite vue app with env variables</p>
    <h1 v-if="isVariable">{{ variable }}</h1>
    <h1 v-else>Failed to load the env variable</h1>
  </div>
</template>
