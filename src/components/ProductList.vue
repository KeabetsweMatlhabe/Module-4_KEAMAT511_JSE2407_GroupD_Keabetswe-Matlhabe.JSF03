<template>
    <div class="product-list">
      <div v-for="product in products" :key="product.id" class="product-card">
        <img :src="product.image" :alt="product.title" class="product-image" />
        <h2>{{ product.title }}</h2>
        <p>\${{ product.price }}</p>
      </div>
    </div>
  </template>
  
  <script>
  import { useProducts } from '../composables/useProducts';
  
  export default {
    setup() {
      const { products } = useProducts();
      return {
        products,
      };
    },
  };
  </script>
  
  <style scoped>
  .product-list {
    display: flex;
    flex-wrap: wrap;
    gap: 16px;
  }
  .product-card {
    border: 1px solid #ddd;
    padding: 16px;
    width: calc(25% - 32px);
    box-sizing: border-box;
  }
  .product-image {
    max-width: 100%;
    height: auto;
  }
  </style>
  