<template>
<!-- <section class="vueMenu">
  <section class="menuNav">
    <button class="menuNavBtn" v-for="(toy, index) in toys" :key="toy.id" @click="selectToy(index)">{{toy.name}}</button>
  </section>
  <div v-if="selectedToy != undefined" id="toyDisplay" @click="resetToy()">
    <h2>{{toys[selectedToy].name}}</h2>
    <img :src="'./assets/img/' + toys[selectedToy].url" alt="">
    <p>{{toys[selectedToy].description}}</p>
  </div>
</section> -->
<FrokostComponent v-if="true"></FrokostComponent>
<IndenMaden v-if="true"></IndenMaden>
<SeasonMenu v-if="true"></SeasonMenu>
<PizzaMenu v-if="true"></PizzaMenu>
<AlaCarte v-if="true"></AlaCarte>
<VinComp v-if="true"></VinComp>
<DrikkevareComp v-if="true"></DrikkevareComp>
</template>

<script>
import FrokostComponent from './components/FrokostComponent.vue'
import IndenMaden from './components/IndenMaden.vue'
import SeasonMenu from './components/SeasonMenu.vue'
import PizzaMenu from './components/PizzaMenu.vue'
import AlaCarte from './components/AlaCarte.vue'
import VinComp from './components/VinComp.vue'
import DrikkevareComp from './components/DrikkevareComp.vue'

export default {
  components: {
    FrokostComponent,
    IndenMaden,
    SeasonMenu,
    PizzaMenu,
    AlaCarte,
    VinComp,
    DrikkevareComp
  }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Titillium+Web:ital,wght@0,200;0,300;0,400;0,600;0,700;0,900;1,200;1,300;1,400;1,600;1,700&display=swap");
#app {
  font-family: "Titillium Web", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.vueMenu {
  display: flex;
}
.menuNav {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  width: 20%;
  margin-top: 5rem;
  padding-left: 8rem;
  border-right: 2px solid #707070;
}
.menuNavBtn{
  background-color: transparent;
  border: none;
  text-align: left;
  font-size: 20px;
  font-weight: normal;
  
  cursor: pointer;
}
</style>
