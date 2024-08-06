<template>
  <div id="app">
    <!-- The Navbar will persist across all pages -->
    <Navbar />
    <!-- The ProductListComponent will display the list of products -->
    <ProductListComponent />
    <!-- The router-view will display the component corresponding to the current route -->
    <router-view />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import ProductListComponent from './components/ProductList.vue';

export default {
  components: {
    Navbar,
    ProductListComponent,
  },
};
</script>
