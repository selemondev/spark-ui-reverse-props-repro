<script setup lang="ts">
import NormalComponent from './components/NormalComponent.vue';
import ReversedComponent from './components/ReversedComponent.vue';
</script>

<template>
  <div class="grid place-items-center min-h-screen w-full">
    <div class="flex flex-col space-y-4">
      <NormalComponent />
      <ReversedComponent />
    </div>
  </div>
</template>
