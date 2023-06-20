<template>
    <section class="car-list">
        <h2>Car List</h2>
        <img src="@/img/avatar.jpeg" alt="">
        <ul>
            <li v-for="car in cars" v-bind:key="car.id">
                <CarPreview :car="car"/>
                <button @click="onRemoveCar(car.id)">x</button>
            </li>
        </ul>
    </section>
</template>

<script>
import CarPreview from './car-preview.vue'

export default {
    props: ['cars'],
    methods: {
        onRemoveCar(carId) {
            const idx = cars.findIndex(car => car.id === carId)
            this.cars.splice(idx, 1)
        }
    },
    components: {
        CarPreview,
    },
}
</script>

<style lang="scss">

.car-list ul {
    display: grid;
    gap: 10px;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr) );
    list-style-type: none;

    padding: 1em;
    background-color: lightblue;
}
.car-list ul li {
    display: grid;
    padding: 10px;
    background-color: lightgoldenrodyellow;

    button {
        place-self: end;
    }
}
</style>