<!-- /products -->
<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="individualProd in products">
                <ProductCard :product="individualProd"/>
            </div>
        </div>
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'products'
    })
    //fetch the products
    const { data: products } = await useFetch('https://fakestoreapi.com/products');

    useHead({
        title: 'Nuxt test | Merch',
        meta: [
            { name: 'description', content: 'Nuxt 3 text merch' }
        ]
    })

</script>

<style scoped></style>