<script setup lang="ts">
import { ref } from "vue";
import { DragSelect, DragSelectOption } from "@coleqiu/vue-drag-select";

const selection = ref(["item1"]);
const options = ["item1", "item2", "item3"];
</script>

<template>
  <drag-select v-model="selection">
    <drag-select-option v-for="item in options" :value="item" :key="item">{{
      item
    }}</drag-select-option>
  </drag-select>
</template>

<style>
.drag-select-option {
  width: 100px;
  height: 100px;
  color: #ffffff;
  background: #e37e26;
}

.drag-select-option--selected {
  color: #000000;
  background: #5fdddc;
}
</style>
