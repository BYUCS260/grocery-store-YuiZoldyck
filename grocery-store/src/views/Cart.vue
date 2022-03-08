<template>
<div>
  <h1>Your Cart</h1>
  <CartList :products="cart" />
  <h2 class="center" v-if="this.$root.$data.cart.length == 0">Please add items into your cart</h2>
</div>
</template>

<script>
import CartList from "../components/CartList.vue"
export default {
  name: 'BrowsePage',
  components: {
    CartList
  },
  data() {
    return {
    }
  },
  computed: {
    cart() {
      return this.$root.$data.cart;
    }
  },
  methods: {
    
  }
}
</script>


<style scoped>
.center {
  text-align: center;
}
</style>