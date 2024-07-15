<script setup>
  import { defineProps } from 'vue';

  defineProps({
    title: {
      type: String,
      required: true,
    },
  });
</script>

<template>
  
  <div class="Card">
    <h1>{{ title }}</h1>
    <slot>
      <p>conteudo do card padrao</p>
    </slot>
  </div>
  
</template>

<style scoped>
  .card {
    padding: 20px;
    border: 1px solid gray;
    border-radius: 5px;
    box-shadow: 3px 3px 2px 2px gray;
  }
</style>