<template>
    <div>
        <h1>Your Cart</h1>

        <CartItemCard 
            v-for="product in products"
            :key="product.id"
            :product="product" />

    </div>
</template>


<script>
import CartItemCard from '../components/cart/CartItemCard.vue'

export default {
    components: {
        CartItemCard
    },
    computed: {
        products() {
            return this.$store.getters.cartItems
        }
    }
}
</script>

<style lang="scss">
.cart-item-card {
    width: 90%;
    margin: 5%;
    background-color: rgb(255, 255, 255);
    box-shadow: 0 0 5px rgb(180, 88, 88);
    border-radius: 5px;
    padding: 10px;
    text-align: left;

    .header {
        display: flex;
        justify-content: space-around;
    }
}
</style>