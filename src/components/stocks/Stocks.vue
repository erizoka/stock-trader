<template>
    <v-layout row wrap>
        <Stock v-for="stock in stocks" :key="stock.id" :stock="stock"/>
    </v-layout>
</template>

<script>
import Stock from './Stock.vue';

export default {
    components: {Stock},
    computed: {
        stocks(){
            return this.$store.getters.stocks
        }
    }
}
</script>

<style>
    
</style>