<template>
    <article class="car-preview">
        <h2>{{ car.vendor }}</h2>
        <h3>{{ car.speed }}</h3>
    </article>
</template>

<script>
export default {
    props: ['car']
}
</script>

<style lang="scss">
</style>