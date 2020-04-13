<template>
  <div id="form">
      <div id=texto>
     <input id="text" type="text" placeholder="Nova tarefa" class="caixa" v-model="titulo">
        <button @click="adicionaTarefa">OK</button>

      </div>
  </div>

</template>

<script>
export default {
  name: "TodoForm",
  data: function(){
  return{
    titulo: ''
  }
  }, methods: {
    adicionaTarefa: function(){
      this.$emit('adicionaTarefa', {titulo: this.titulo})
     
    }

    }
  }


</script>

<style>
#form{
    width: 400px;
    height: 150px;
    border: 1px solid #ffffff;
    margin: 170px auto 50px auto;
    display: flex;
    flex-wrap: wrap;

}
#text{
padding: 10px;
margin: auto 5px 0 auto;
}
#texto{
    width: 60px;
    height: 60px;
    margin-top: 34px;
    margin-left: 100px;
}
.bnt_ok{
  text-align: center;
  background: burlywood;
  
}
</style>