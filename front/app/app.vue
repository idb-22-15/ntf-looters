<script setup lang="ts">
import '~/src/shared/assets/css/tailwind.css'
import { Toaster } from '~/src/shared/ui/kit/toast'
</script>

<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
  <Toaster />
</template>
<!-- eslint-disable vue/enforce-style-attribute -->

<style>
@import url('https://fonts.googleapis.com/css2?family=Onest:wght@100..900&display=swap');
</style>
