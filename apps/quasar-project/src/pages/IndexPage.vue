<template>
  <q-page class="row items-center justify-evenly">
    <example-component
      title="Example component"
      active
      :products="products"
    ></example-component>
  </q-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';

import { Product } from '@felip-store/core';
import ExampleComponent from 'components/ExampleComponent.vue';

const products = ref<Product[]>([
  {
    id: 1,
    name: 'Hijab 1',
    price: 2.4,
  },
  {
    id: 2,
    name: 'Hijab 2',
    price: 2.4,
  },
  {
    id: 3,
    name: 'Hijab 3',
    price: 2.4,
  },
]);
</script>
