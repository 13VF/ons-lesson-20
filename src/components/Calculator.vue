<template>
  <div class="calculator">
    <h1>{{ msg }} {{ number }}</h1>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'Calculator',
  props: {
    msg: String, // 123
    number: Number,
  },
});
</script>

<style scoped>
.calculator {
  display: flex;
}
</style>
