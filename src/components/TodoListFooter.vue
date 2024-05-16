<script setup lang="ts">
  import { useRoute } from 'vue-router'

  const route = useRoute()

  const year: number = new Date().getFullYear()
</script>

<template>
  <div class="flex flex-col items-center mt-4">
    <router-link
      v-if="route.name === 'todoList'"
      class=""
      :to="{ name: 'about' }"
    >
      
    </router-link>
    <router-link
      v-if="route.name === 'about'"
      class=""
      :to="{ name: 'todoList' }"
    >
      TodoList
    </router-link>

    <p class="mt-2 text-sm text-zinc-500">
      
    </p>
  </div>
</template>
