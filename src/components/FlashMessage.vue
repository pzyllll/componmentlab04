<!-- src/components/FlashMessage.vue -->

<template>
  <div class="flash-message" v-if="message">
    <p>{{ message }}</p>
    <button @click="$emit('close')">Close</button>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  message: string
}>();

defineEmits(['close']);
</script>

<style scoped>
.flash-message {
  background-color: #d4edda;
  border: 1px solid #c3e6cb;
  color: #155724;
  padding: 10px;
  margin: 10px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.flash-message p {
  margin: 0;
}
</style>
