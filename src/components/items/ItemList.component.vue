<template>
  <h3>Item Lists</h3>
  <ul>
    <li v-for="item in items" :key="item.id">
      {{item.name}}
    </li>
  </ul>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import { ItemInterface } from '@/models/items/Item.interface'
export default defineComponent ({
  props : {
    items : {
      type: Array as PropType<ItemInterface[]>
    }
  }
})
</script>

<style>

</style>