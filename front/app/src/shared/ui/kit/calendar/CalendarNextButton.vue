<script lang="ts" setup>
import { ChevronRight } from 'lucide-vue-next'
import { CalendarNext, useForwardProps, type CalendarNextProps } from 'radix-vue'
import { computed, type HTMLAttributes } from 'vue'

import { cn } from '~/src/shared/lib/utils'
import { buttonVariants } from '~/src/shared/ui/kit/button'

const props = defineProps<CalendarNextProps & { class?: HTMLAttributes['class'] }>()

const delegatedProps = computed(() => {
  const { class: _, ...delegated } = props

  return delegated
})

const forwardedProps = useForwardProps(delegatedProps)
</script>

<template>
  <CalendarNext
    :class="cn(
      buttonVariants({ variant: 'outline' }),
      'h-7 w-7 bg-transparent p-0 opacity-50 hover:opacity-100',
      props.class,
    )"
    v-bind="forwardedProps"
  >
    <slot>
      <ChevronRight class="h-4 w-4" />
    </slot>
  </CalendarNext>
</template>
