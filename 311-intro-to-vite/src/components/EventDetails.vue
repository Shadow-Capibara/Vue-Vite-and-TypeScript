<!-- src/components/EventDetails.vue -->
<script setup lang="ts">
import { defineProps } from 'vue';
import { Event } from '@/types/Event';

defineProps<{
  event: Event
}>();
</script>

<template>
  <div class="event-details">
    <h2 class="category">{{ event.category }}</h2>
    <span class="organizer">{{ event.organizer }}</span>
  </div>
</template>

<style scoped>
.event-details {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  font-size: 16px;
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}

.category, .organizer {
  margin-bottom: 4px;
}
.event-details:hover{
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2)
}
</style>
