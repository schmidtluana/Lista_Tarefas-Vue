<template>
  <div id="app">
    <TodoForm :tarefas="tarefas" @adicionaTarefa="adicionouTarefa($event)"/>
    <TodoList :tarefas="tarefas"/>
    <div id=caixa></div>
     <div id="titulo">
      <h1>Lista de Tarefas</h1>
    </div>

  </div>
</template>

<script>
import TodoForm from "./components/TodoForm"
import TodoList from "./components/TodoList"

export default {
  name: 'App',
  components:{
    TodoList,
    TodoForm

  }, data: function(){
    return{
    tarefas: []    
};
  }, methods: {
    adicionouTarefa: function(event){
      this.tarefas.push({texto: event.titulo});
    }
  }
}

</script>

<style>
#titulo{
  color: beige;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  margin-top: -466px;
  margin-left: 550px;

}
#caixa{
  width: 500px;
  height: 440px;
  border: solid floralwhite 5px;
  margin-top: -440px;
  margin-left: 418px;
}

</style>