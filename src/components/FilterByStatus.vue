<template>
    <div class="filter">
        <div class="items" @click="filter('')">
            All
        </div>
        <div class="items" @click="filter('Alive')">
            Alive
        </div>
        <div class="items" @click="filter('Dead')">
            Dead
        </div>
        <div class="items" @click="filter('unknown')">
            Unknown 
        </div>
    </div>
</template>

<script>
import { useStore } from 'vuex'
export default {
    setup() {
        const store = useStore()
    
        const filter = ((status) => {
            store.dispatch('filterByStatus', status)
        })

        return {
            filter
        }
    }
}
</script>

<style lang="scss">

.filter {
    width: 400px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    border-radius: 10px;
    overflow: hidden;
    .items {
        padding: 1rem 0.5rem;
        background-color: rgb(73, 58, 58);
        text-align: center;
        cursor: pointer;
        &:hover {
            color: rgb(223, 48, 4);
        }
    }
} 
</style>