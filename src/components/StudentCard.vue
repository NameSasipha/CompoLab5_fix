<template>

    <div class=" text-lime-100 mt-5 pt-3 text-center border-2 border-green-50 w-42 h-20 ">
      <span> {{ event?.name }} </span>
      <span> {{ event?.surname }} </span>
      <h4>{{ event?.gpa}}</h4>
    </div>

</template>

<script setup lang="ts">
import type { StudentItem } from '@/type'
import type { PropType } from 'vue'
const props = defineProps({
    event:{
        type: Object as PropType<StudentItem>,
            require: true
    }
})

</script>

<style scoped>
/* .event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}

.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12 px 0 rgba(0, 0, 0, 0.2);
} */
</style>
