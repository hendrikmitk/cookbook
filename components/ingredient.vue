<script setup>
const props = defineProps({
  name: String,
  quantity: Number | String,
  type: String,
  underline: { type: Boolean, default: false },
  units: String,
});
</script>

<template>
  <span :class="{ ingredient: underline }">
    <IngredientQuantity :quantity="quantity" :units="units" /> {{ name }}
  </span>
</template>

<style scoped>
.ingredient {
  display: inline-block;
  text-decoration: underline;
}

.ingredient::first-letter {
  text-transform: lowercase;
}
</style>
