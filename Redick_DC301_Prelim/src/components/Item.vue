<script setup>
import ItemList from './ItemList.vue'
</script>

<template>
const itemCounter = mount(ItemList)
expect(itemCounter.isVisible()).toBe(true)
expect(itemCounter.find('.is-not-visible').isVisible()).toBe(false)
</template>