<template>
  <div class="card">
      <a :href="item.href">
        <img :src="item.img" alt="Icone servico"/>
        <span>{{ item.titulo }}</span> 
     </a>
  </div>
</template>

<script>
export default {
    props:['item']
}
</script>

<style scoped>
    div{
        display: block;
        width: 100px;
        margin: 20px 50px 20px 50px;
    }
    img{
        max-width: 4rem;
        
    }
    span{
        font-weight: 900;
    }
    a{
        text-decoration: none;
        color: rgb(255, 255, 255);
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
        align-items: center;
    }
    .card{
        display: flex;
        justify-content: center;
        flex-direction: column;
        min-width: 130px;
        min-height: 160px;
        border: 1px solid grey;
        border-radius: 5%;
        box-shadow: 0 0 2em grey;
        opacity: .9;
        transition: box-shadow .5s;
        background-color: rgba(39, 38, 38, 0.438);
    }
    .card:hover{
        opacity: 1;
         box-shadow: 0 0 4em rgb(92, 91, 91);
    }
</style>