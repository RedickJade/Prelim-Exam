<script setup>
import Item from './Item.vue'
</script>

<template>
    <div class="tags-wrapper">
      <p v-for="(filter, index) in filters" :key="index">
        <span
          @click="filterTodo(filter)"
           :class="{ active: filter === activeFilter }"
        >{{ filter }}</span>
      </p>
    </div>

export default {
    setup() {
      const filters = ref(['All', 'Personal', 'Work', 'Other']);
      const activeFilter = ref('All');
      
      return {
        filters,
        activeFilter
      }
    }
  }
</template>