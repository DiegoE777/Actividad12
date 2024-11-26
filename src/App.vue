<template>
  <div id="app">
    <h1>Chuck Norris Jokes</h1>
    <ul>
      <li v-for="(joke, index) in jokes" :key="index">{{ joke.value }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      jokes: [
        { value: "Chuck Norris can skydive into outer space." },
        { value: "The chief export of Chuck Norris is pain." },
        { value: "Chuck Norris doesn't read books. He stares them down until he gets the information he wants." },
        { value: "Time waits for no man. Unless that man is Chuck Norris." },
        { value: "If you spell Chuck Norris in Scrabble, you win. Forever." }
      ]
    };
  }
};
</script>

<style scoped>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 50px;
}

h1 {
  color: #333;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  background-color: #f4f4f4;
  margin: 5px;
  padding: 10px;
  border-radius: 5px;
}
</style>
