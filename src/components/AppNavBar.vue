<template>
  <nav>
    <button @click="test">Button #1</button>
    <button>Button #2</button>
    <button>Button #3</button>
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
