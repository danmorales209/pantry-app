<template>
  <nav>
    <button @click="test">Bind TEst</button>
    <button @click="httpTest">Server TEst</button>
    <button @click="debugInfo">DEBUG</button>
  </nav>
</template>

<script>
export default {
  name: "AppNavBar",
  data: () => {
    return {
      dummy: "This is some test data"
    };
  },
  methods: {
    test: function() {
      console.log(this.$data.dummy);
    },
    httpTest: function() {
      return this.$http.get("http://localhost:3001/").then(results => {
        console.log(results);
      });
    },
    debugInfo: function() {
      console.log(this);
    }
  }
};
</script>

<style scoped>
nav {
  background-color: #456456;
}

button {
  background-color: white;
  color: black;
}
</style>
