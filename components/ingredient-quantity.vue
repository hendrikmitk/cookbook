<script setup>
import { prettyFractions } from '~/utils/pretty-fractions';
const props = defineProps(['quantity', 'units']);

const sanitizeQuantity = (rawQuantity) => {
  if (!isNaN(Number(rawQuantity))) {
    return prettyFractions(rawQuantity);
  } else {
    return 'Etwas';
  }
};
</script>

<template>
  {{ sanitizeQuantity(quantity) }} {{ units }}
</template>
