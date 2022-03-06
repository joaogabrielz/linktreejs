<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup

import Item from './components/Item.vue';
import Footer from './components/Footer.vue'
</script>

<script>
import Dados from './Dados/Services.json';

export default {
  data(){
    return{
      servicos:null
    }
  },
  mounted(){
    this.servicos = Dados;
  //   console.log(Dados);
   }
}
</script>

<template>
  <img alt="Vue logo" style="width:150px" src="./assets/fotujoao.jpg" />
  <h1>Seja Bem vindo(a)!</h1>
  <hr/>
  <div class="items">
      <Item 
        v-for="servico, index in servicos"
        :key="index"
        :item="servico"
      />

  </div>

  <Footer />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body{
  background: url("https://wallpaperaccess.com/full/187161.jpg");
  background-repeat:no-repeat ;
  background-size:cover;
  min-height: 100%;
  opacity: 99%;
}
.items{
  display: flex;
  justify-content: center;
  flex-wrap:wrap ;
}
h1{
  color: rgb(233, 230, 230);
}
</style>
