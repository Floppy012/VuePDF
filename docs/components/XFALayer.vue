<script setup>
import { VuePDF, usePDF } from '@tato30/vue-pdf'
import { withBase } from '@vuepress/client'
import '@tato30/vue-pdf/style.css'

const { pdf } = usePDF({
  url: withBase('/example_xfa.pdf'),
  enableXfa: true,
})
</script>

<template>
  <div class="container">
    <VuePDF :pdf="pdf" />
  </div>
</template>
