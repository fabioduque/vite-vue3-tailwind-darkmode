<script setup>
  import { ref, watchEffect } from "vue"
  
  const darkMode = ref(document.body.classList.contains('dark'));
  const applyDarkMode = () => document.body.classList[
    darkMode.value ? 'add' : 'remove'
  ]('dark');
  watchEffect(applyDarkMode);
    
</script>

<template>
  <div>
    <h1 class="mb-9 p-5 text-5xl font-bold dark:text-slate-50 dark:bg-slate-500 text-slate-900 bg-slate-200">Hello World</h1>
  </div>
  <label for="">Activate dark mode</label>
  <br />
  <input type="checkbox" name="" id="" v-model="darkMode">
</template>

<style>
</style>
