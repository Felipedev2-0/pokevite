<script setup>
const pokemon = defineProps(["name", "urlBaseSvg"])

</script>


<template>
    <div class="col-4">
        <div class="card p-2 mb-3 cardListPokemon">
            <p class="text-center">{{ pokemon.name }}</p>
            <img :src="urlBaseSvg" class="card-img-top" alt="..." height="80" />
        </div>
    </div>
</template>

<style scoped>
.cardListPokemon {
    background: rgb(31, 64, 230);
    background: radial-gradient(circle, rgba(46, 71, 196, 0.5) 0%, rgba(194, 31, 64, 0.3) 100%);
    cursor: pointer;
}

.cardListPokemon :hover{
    background: rgb(31, 64, 230);
    background: radial-gradient(circle, rgba(31, 64, 230, 0.6) 0%, rgba(204, 14, 52, 0.4) 100%);
    cursor: pointer;
}

.cardListPokemon img:hover{
   padding: .1rem;
}
</style>