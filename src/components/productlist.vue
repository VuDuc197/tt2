<template>
  <div>
    <h2>Product List</h2>
    <product-list :products="products" @add-to-cart="addToCart"></product-list>
  </div>
</template>

<script>
import ProductList from './ProductList.vue';

export default {
  name: 'App',
  components: {
    'product-list': ProductList
  },
  data() {
    return {
      products: [
        {
          id: 1,
          name: 'Product 1',
          description: 'This is product 1',
          price: 10
        },
        {
          id: 2,
          name: 'Product 2',
          description: '