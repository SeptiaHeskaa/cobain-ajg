<script setup lang="ts">
  import { reactive } from 'vue'

  interface Props {
    active: string
  }

  const { active } = defineProps<Props>()

  const emit = defineEmits(['toggle-active'])

  const tabOptions: string[] = ['all', 'todo', 'done']
</script>

<template>
  <div class="flex mt-4">
    <div
      v-for="item in tabOptions"
      :key="item"
      class="grow py-1 text-center text-red-700 uppercase rounded-t-lg border-solid border-b-2 border-red-700 cursor-pointer transition duration-300"
      :class="{ '!text-teal-100 bg-red-700': item === active }"
      @click.prevent="emit('toggle-active', item)"
    >
      {{ item }}
    </div>
  </div>
</template>
