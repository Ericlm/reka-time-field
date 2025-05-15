<script setup lang="ts">
import { TimeFieldInput, TimeFieldRoot } from 'reka-ui'
</script>

<template>
  <div class="max-w-xl mx-auto">
    <label for="time" class="block mt-8 text-sm/6 font-medium text-gray-900">Time</label>
    <TimeFieldRoot
      class="mt-2 inline-flex w-full rounded-md bg-white px-3 py-1.5 text-base text-gray-900 outline-1 -outline-offset-1 outline-gray-300 placeholder:text-gray-400 focus:outline-2 focus:-outline-offset-2 focus:outline-indigo-600 sm:text-sm/6"
      locale="fr"
      id="time"
      v-slot="{ segments }"
    >
      <template v-for="item in segments" :key="item.part">
        <TimeFieldInput :part="item.part">
          {{ item.value }}
        </TimeFieldInput>
      </template>
    </TimeFieldRoot>
  </div>
</template>
