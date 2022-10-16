<template>
  <v-container>
    <v-text-field></v-text-field>
    <v-jsf v-model="model" :schema="schema" :options="options"></v-jsf>
  </v-container>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'VuetifyTestPage',
  data: () => ({
    valid: false,
    model: {},
    schema: {
      type: 'object',
      properties: {
        stringProp: { type: 'string' },
        colorProp: { type: 'string', 'x-display': 'color-picker' },
      }
    }
  })
})
</script>
