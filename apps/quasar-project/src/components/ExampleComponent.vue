<template>
  <div>
    <p>New Products</p>

    <q-card v-for="product in products" :key="product.id" class="my-card">
      <q-img src="https://cdn.quasar.dev/img/parallax2.jpg">
        <div class="absolute-bottom text-h6">{{ product.name }}</div>
      </q-img>

      <q-card-section>
        {{ product.price }}
      </q-card-section>
    </q-card>
  </div>
</template>

<script setup lang="ts">
import { Product } from '@felip-store/core';

interface Props {
  products?: Product[];
}
const props = withDefaults(defineProps<Props>(), {
  products: () => [],
});
</script>
