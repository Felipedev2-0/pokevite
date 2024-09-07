<script setup>

const pokemon = defineProps(["name", "xp", "height","img", "loading"])

</script>

<template>
  <div class="card cardPokemonSelected"
  :class="loading ? '' : 'animate__animated animate__flipInY'"
  >

    <img
      :src="pokemon.img"
      height="250"
      class="card-img-top pt-2"
       :alt="pokemon.name">

    <div class="card-body">
      <h5 class="card-title text-center">{{ pokemon.name }}</h5>
      <hr>
     <div class="row">
      <section class="col">
        <strong>XP:</strong>
        <span>{{ pokemon.xp }}</span>
      </section>
      <section class="col">
        <strong>Altura:</strong>
        <span>{{ pokemon.height }}</span>
      </section>
     </div>
    </div>
  </div>
</template>


<style scoped>
.cardPokemonSelected{
  height: 450px;
  background: rgb(31, 64, 230);
  background: radial-gradient(circle, rgba(58, 68, 4, 0.5) 0%, rgba(0, 0, 0, 0.3) 100%);
}

</style>