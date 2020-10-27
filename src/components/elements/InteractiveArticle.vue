<template>
  <article class="font-light text-2xl leading-loose lg:leading-relaxed">
    <interactive-document
      v-for="child in article.children"
      :key="child._id"
      :document="child"
    />
  </article>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'

import { Parent } from 'docci'

export default defineComponent({
  name: 'InteractiveArticle',
  props: {
    article: {
      type: Object as PropType<Parent>,
      required: true,
    },
  },
})
</script>
