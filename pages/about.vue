<template>
    <div>
        <h2>About Page</h2>
        <p>About Paragraph</p>
        <div>{{ data }}</div>
    </div>
</template>

<script setup>
    // const { data } = await useFetch('/api/ninja');
    // const { data } = await useFetch('/api/ninja?name=personsName', {
    //     method: 'post',
    //     body: { age: 27 }
    // });

    const { data } = await useFetch('/api/currency/INR')
</script>

<style scoped>
h2 {
    margin-bottom: 20px;
    font-size: 36px;
}
p {
    margin: 20px 0;
}
</style>