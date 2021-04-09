<template>
  <div class="container">
    <p class="d-none">{{ getData() }}</p>
    <div class="row mb-4" v-for="(personaje, i) in character" :key="i">
      <div class="col-6">
        <img class="pic" :src="personaje.image" alt="" />
      </div>
      <div class="col-6 my-auto">
        <h3 class="text-start fs-1 text-success name-title">
          {{ personaje.name }}
        </h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Personajes",
  data() {
    return {
      character: [],
    };
  },
  methods: {
    async getData() {
      const url = "https://rickandmortyapi.com/api/character";
      try {
        const req = await fetch(url);
        const reqJson = await req.json();
        // console.log(reqJson.results);
        this.character = reqJson.results;
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>

<style scoped>
.mainTitle {
  color: white;
}
.pic {
  width: 10rem;
  border-radius: 50%;
}
.name-title {
  -webkit-text-stroke-width: 0.25px;
  -webkit-text-stroke-color: white;
}
</style>
