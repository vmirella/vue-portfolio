<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'HomeHeaderItem',
  props: {
    text: {
      type: String,
      required: true,
    },
  },
})
</script>

<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <RouterLink
    class="group/item relative rounded-full px-4 py-2 text-stone-300 hover:text-white"
    to="/"
    >{{ text }}
    <div
      class="invisible absolute -top-[13.25px] left-1/2 h-1 w-8 -translate-x-1/2 rounded-t-full bg-stone-100 group-focus/item:visible"
    ></div>
    <div
      class="invisible absolute -top-[11.25px] left-1/2 h-6 w-12 -translate-x-1/2 rounded-full bg-stone-100/30 blur-md group-focus/item:visible"
    ></div>
    <div
      class="invisible absolute -top-[12.25px] h-6 w-8 rounded-full bg-stone-100/30 blur-md group-focus/item:visible"
    ></div>
    <div
      class="invisible absolute -top-[13.25px] left-1/2 h-4 w-4 -translate-x-1/2 rounded-full bg-stone-100/30 blur-sm group-focus/item:visible"
    ></div>
  </RouterLink>
</template>
