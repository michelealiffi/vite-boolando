<script>
import products from '../data/db.json';
import ProductElement from "./AppElement.vue"
export default {
    name: "AppMain",
    data() {
        return {
            products: products.products,
        }
    },
    components: {
        AppElement
    }
}
</script>

<template>
    <div class="container" id="container">
        <div class="row">
            <AppElement v-for="(product, i) in products" :key="product.id" :firstImage="product.frontImage"
                :secondImage="product.backImage" :brand="product.brand" :title="product.name" :price="product.price"
                :heart="product.isInFavorites" :badges="product.badges" :id="product.id" />
        </div>
    </div>
</template>