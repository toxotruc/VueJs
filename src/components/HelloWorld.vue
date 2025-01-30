<template>
  {{ x }}, {{ y }}
  <div v-if="isDark">Dark mode</div>
  <div v-else>Light mode</div>
</template>

<script setup lang="ts">
import { useMouse, usePreferredDark, useLocalStorage } from '@vueuse/core'

  // tracks mouse position
  const { x, y } = useMouse()

  // is user prefers dark theme
  const isDark = usePreferredDark()
</script>