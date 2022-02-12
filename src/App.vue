<template>
  <div id="app">
    <h1 class="game_header">Игра "Тренируй память"</h1>
    <GameTable :list="items"/>
  </div>
</template>

<script>
import GameTable from "@/components/GameTable";
export default {
  name: "App",
  components: {
    GameTable,
  },
  data() {
    return {
      items: [
        {
          id: 1,
          url: require("./assets/img/new-york.jpeg"),
          card: require("./assets/img/card.png"),
          number: 1,
          status: true,
        },
        {
          id: 2,
          url: require("./assets/img/new-york.jpeg"),
          card: require("./assets/img/card.png"),
          number: 1,
          status: true,
        },
        {
          id: 3,
          url: require("./assets/img/dog.jpeg"),
          card: require("./assets/img/card.png"),
          number: 2,
          status: true,
        },
        {
          id: 4,
          url: require("./assets/img/dog.jpeg"),
          card: require("./assets/img/card.png"),
          number: 2,
          status: true,
        },
        {
          id: 5,
          url: require("./assets/img/kat.jpeg"),
          card: require("./assets/img/card.png"),
          number: 3,
          status: true,
        },
        {
          id: 6,
          url: require("./assets/img/kat.jpeg"),
          card: require("./assets/img/card.png"),
          number: 3,
          status: true,
        },
        {
          id: 7,
          url: require("./assets/img/beach.jpeg"),
          card: require("./assets/img/card.png"),
          number: 4,
          status: true,
        },
        {
          id: 8,
          url: require("./assets/img/beach.jpeg"),
          card: require("./assets/img/card.png"),
          number: 4,
          status: true,
        },
        {
          id: 9,
          url: require("./assets/img/books.jpeg"),
          card: require("./assets/img/card.png"),
          number: 5,
          status: true,
        },
        {
          id: 10,
          url: require("./assets/img/books.jpeg"),
          card: require("./assets/img/card.png"),
          number: 5,
          status: true,
        },
        {
          id: 11,
          url: require("./assets/img/china.jpeg"),
          card: require("./assets/img/card.png"),
          number: 6,
          status: true,
        },
        {
          id: 12,
          url: require("./assets/img/china.jpeg"),
          card: require("./assets/img/card.png"),
          number: 6,
          status: true,
        },
        {
          id: 13,
          url: require("./assets/img/Colosseum.jpeg"),
          card: require("./assets/img/card.png"),
          number: 7,
          status: true,
        },
        {
          id: 14,
          url: require("./assets/img/Colosseum.jpeg"),
          card: require("./assets/img/card.png"),
          number: 7,
          status: true,
        },
        {
          id: 15,
          url: require("./assets/img/more.jpeg"),
          card: require("./assets/img/card.png"),
          number: 8,
          status: true,
        },
        {
          id: 16,
          url: require("./assets/img/more.jpeg"),
          card: require("./assets/img/card.png"),
          number: 8,
          status: true,
        },
        {
          id: 17,
          url: require("./assets/img/mountains.jpeg"),
          card: require("./assets/img/card.png"),
          number: 9,
          status: true,
        },
        {
          id: 18,
          url: require("./assets/img/mountains.jpeg"),
          card: require("./assets/img/card.png"),
          number: 9,
          status: true,
        },
        {
          id: 19,
          url: require("./assets/img/panda.jpeg"),
          card: require("./assets/img/card.png"),
          number: 10,
          status: true,
        },
        {
          id: 20,
          url: require("./assets/img/panda.jpeg"),
          card: require("./assets/img/card.png"),
          number: 10,
          status: true,
        },
        {
          id: 21,
          url: require("./assets/img/pyramids.jpeg"),
          card: require("./assets/img/card.png"),
          number: 11,
          status: true,
        },
        {
          id: 22,
          url: require("./assets/img/pyramids.jpeg"),
          card: require("./assets/img/card.png"),
          number: 11,
          status: true,
        },
        {
          id: 23,
          url: require("./assets/img/sea.jpeg"),
          card: require("./assets/img/card.png"),
          number: 12,
          status: true,
        },
        {
          id: 24,
          url: require("./assets/img/sea.jpeg"),
          card: require("./assets/img/card.png"),
          number: 12,
          status: true,
        },
        {
          id: 25,
          url: require("./assets/img/ship.jpeg"),
          card: require("./assets/img/card.png"),
          number: 13,
          status: true,
        },
        {
          id: 26,
          url: require("./assets/img/ship.jpeg"),
          card: require("./assets/img/card.png"),
          number: 13,
          status: true,
        },
        {
          id: 27,
          url: require("./assets/img/tower.jpeg"),
          card: require("./assets/img/card.png"),
          number: 14,
          status: true,
        },
        {
          id: 28,
          url: require("./assets/img/tower.jpeg"),
          card: require("./assets/img/card.png"),
          number: 14,
          status: true,
        },
        {
          id: 29,
          url: require("./assets/img/wood.jpeg"),
          card: require("./assets/img/card.png"),
          number: 15,
          status: true,
        },
        {
          id: 30,
          url: require("./assets/img/wood.jpeg"),
          card: require("./assets/img/card.png"),
          number: 15,
          status: true,
        },
      ]
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.game_header{
  font-weight: 700;
  font-size: 40px;
}
</style>
