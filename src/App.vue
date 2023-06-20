<script>
import CarList from './cmps/car-list.vue'

export default {
    data() {
        return {
            cars: [
                { id: 'c101', vendor: 'Subalu', speed: 110 },
                { id: 'c102', vendor: 'Fiak', speed: 130 },
                { id: 'c103', vendor: 'Suzuzu', speed: 20 },
                { id: 'c104', vendor: 'Susila', speed: 160 },
            ]
        }
    },
    components: {
        CarList
    }
}
</script>

<template>
    <header> 
        <h1>Hello Vue + Vite</h1>
    </header>
    <main>
        <CarList :cars="cars"/>
    </main>
</template>

<style>
</style>
