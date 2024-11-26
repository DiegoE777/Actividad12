<template>
  <div id="app" class="container">
    <h1 class="text-center my-4">Chuck Norris Jokes</h1>
    <div class="row">
      <chuck-card
        v-for="(joke, index) in jokes"
        :key="index"
        :icon_url="joke.icon_url"
        :value="joke.value"
        class="col-md-4 mb-4"
      />
    </div>
  </div>
</template>

<script>
import ChuckCard from './components/ChuckCard.vue';

export default {
  name: "App",
  components: {
    ChuckCard
  },
  data() {
    return {
      jokes: [
        { 
          icon_url: "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          value: "Chuck Norris can skydive into outer space." 
        },
        { 
          icon_url: "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          value: "The chief export of Chuck Norris is pain." 
        },
        { 
          icon_url: "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          value: "Chuck Norris doesn't read books. He stares them down until he gets the information he wants." 
        },
        { 
          icon_url: "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          value: "Time waits for no man. Unless that man is Chuck Norris." 
        },
        { 
          icon_url: "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          value: "If you spell Chuck Norris in Scrabble, you win. Forever." 
        }
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

.row {
  display: flex;
  flex-wrap: wrap;
}

@media (max-width: 767px) {
  .col-md-4 {
    flex: 0 0 100%;
  }
}
</style>
