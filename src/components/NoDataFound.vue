<script setup lang="ts">
import image from '@images/misc/teamwork.png'

const props = defineProps<Props>()

interface Props {
  errorCode?: string
  errorTitle?: string
  errorDescription?: string
}
</script>

<template>
  <VEmptyState
    :image="image"
    size="250"
  >
    <template #title>
      <div class="mt-8 text-2xl">
        {{ props.errorTitle }}
      </div>
    </template>

    <template #text>
      <div class="text-subtitle">
        {{ props.errorDescription }}
      </div>
    </template>

    <template #actions>
      <slot name="button" />
    </template>
  </VEmptyState>
</template>
