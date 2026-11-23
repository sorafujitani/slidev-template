<script setup lang="ts">
import { useNav } from '@slidev/client'

interface Props {
  tag?: 'h1' | 'h2' | 'h3'
  animated?: boolean
}

withDefaults(defineProps<Props>(), {
  tag: 'h1',
  animated: false,
})

const { isPrintMode } = useNav()
</script>

<template>
  <component
    :is="tag"
    :class="isPrintMode ? 'print-heading' : ['gradient-heading', { 'animated-shadow': animated }]"
  >
    <slot />
  </component>
</template>

<style scoped>
.print-heading {
  color: var(--color-primary);
}
</style>
