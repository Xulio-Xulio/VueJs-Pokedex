<template>
  <div class="searchbar">
    <form @submit.prevent="setPokemonUrl">
      <input
        class="search"
        placeholder="search"
        type="text"
        v-model="searchvalue"
      />
      <button><i class="fas fa-search" @click="setPokemonUrl"></i></button>
    </form>
  </div>
</template>

<script>
export default {
  props: ["apiUrl"],
  data: () => {
    return {
      searchvalue: "",
    };
  },
  methods: {
    setPokemonUrl(url) {
      if (this.searchvalue !== "")
        this.$emit("setPokemonUrl", this.apiUrl + this.searchvalue);
      console.log(url);
    },
  },
};
</script>

<style>
.searchbar {
  position: relative;
  width: 100%;
  max-width: 510px;
  padding-bottom: 20px;
}

input {
  border: none;
  outline: none;
  border-radius: 5px;
  padding: 10px 40px 10px 10px;
  margin: 10px;
  width: calc(100% - 50px);
  font-size: 1rem;
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2), 0 10px 10px rgba(0, 0, 0, 0.2);
}

button {
  outline: none;
  border: none;
  border-radius: 30px;
  background-color: #d1d1d1;
  color: #efefef;
  padding: 10px 0;
  width: calc(100% - 50px);
  margin-bottom: 20px;
  font-size: 1.2rem;
}

button:hover {
  background-color: #cacacf;
  cursor: pointer;
}
</style>
