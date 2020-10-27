<template>
  <blockquote class="text-content border-l-4 border-blue-100 px-4 my-4">
    <interactive-document
      v-for="child in blockquote.children"
      :key="child._id"
      :document="child"
    />
  </blockquote>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'

import { Blockquote } from 'docci'

export default defineComponent({
  name: 'InteractiveBlockquote',
  props: {
    blockquote: {
      type: Object as PropType<Blockquote>,
      required: true,
    },
  },
})
</script>
