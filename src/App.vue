<template>
<div>
  <button v-for="(toy, index) in toys" :key="toy.id" @click="selectToy(index)">{{toy.name}}</button>
  <div v-if="selectedToy != undefined" id="toyDisplay" @click="resetToy()">
    <h2>{{toys[selectedToy].name}}</h2>
    <img :src="'./assets/img/' + toys[selectedToy].url" alt="">
    <p>{{toys[selectedToy].description}}</p>
  </div>
</div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      toys: [
      {
        "id": 2,
        "name": "All-stars Rubber Ball",
        "description": "It rolls, it bounces, it makes the crowd proud.",
        "url": "02-toy-ball.jpg"
    },
    {
        "id": 4,
        "name": "Evergreen Wooden Blocks with Alphabet",
        "description": "Stack 'em, move 'em, spell 'em: true classics never die hard.",
        "url": "04-toy-blocks.jpg"
    },
    {
        "id": 8,
        "name": "Edward Bear",
        "description": "Hello, my name is Edward Bear, but you may call me Teddy.",
        "url": "08-toy-teddy.jpg"
    },
    {
        "id": 12,
        "name": "I. R. Robot",
        "description": "Rrrr. Whirr. Zing. Klang. I. Rrrr. Robot. U. Rrrr. Friend. Whizz. Plunk. Thud.",
        "url": "12-toy-robot.jpg"
    },
    {
        "id": 15,
        "name": "Seaside Architect Starter Kit",
        "description": "The perfect set for the perfect little architect.",
        "url": "15-toy-sand-bucket.jpg"
    },
    {
        "id": 20,
        "name": "Penny Pingle",
        "description": "Penny Pingle, a pure palpable princess to perfectly partake any picnic in the park.",
        "url": "20-toy-doll.jpg"
    }
      ],
      selectedToy: 1
    };
  },
  methods: {
    selectToy(index){
      this.selectedToy = index;
    },
    resetToy(){
      this.selectedToy = undefined;
    }
  }
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
</style>
