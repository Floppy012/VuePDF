<script setup>
import { VuePDF, usePDF } from '@tato30/vue-pdf';
import { withBase } from '@vuepress/client';
import { ref } from 'vue';

const annotation_layer = ref(false)
const { pdf } = usePDF(withBase('/example_014.pdf'))
</script>

<template>
  <div class="container">
    <div>
      <button class="button-example" @click="annotation_layer = !annotation_layer">
        Change to <strong>{{ !annotation_layer }}</strong>
      </button>
    </div>
    <VuePDF :pdf="pdf" :annotation-layer="annotation_layer" />
  </div>
</template>
