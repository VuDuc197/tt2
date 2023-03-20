<template>
    <div class ="product-list">

    </div class="product" v-for="product in products" :key="product.id">
    <h3> {{ product.name }}</h3>
    <p> {{ product.description }}</p>
    <p>Price: {{ product.price }}</p>
    <button @click="addToCart(product)"> Add to Cart</button>
    <div>

    </div>
</template>
<script>
export default {
  name: 'ProductList',
  props: {
    products: {
      type: Array,
      required: true
    }
  },
  methods: {
    addToCart(product) {
      // emit an event to the parent component to add the product to the cart
      this.$emit('add-to-cart', product);
    }
  }
};
</script>

<style>
.product-list {
  display: flex;
  flex-wrap: wrap;
}

.product {
  flex: 1 1 300px;
  margin: 10px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
</style>