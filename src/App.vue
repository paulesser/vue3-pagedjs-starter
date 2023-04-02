<template>
  <div>
   <button @click="previewer.preview(config.content, config.stylesheets, config.renderTo)" class="no-print"> Run Pagedjs </button>
  </div>
</template>
<script setup>
import { Previewer } from 'pagedjs'
const config = {
  auto: false,
  before: undefined,
  after: undefined,
  content: undefined,
  stylesheets: undefined,
  renderTo: undefined,
  settings: undefined
}
const previewer = new Previewer(config.settings)
</script>
<style scoped>
@media print {
  .no-print {
    display: none;
  }
}

</style>
