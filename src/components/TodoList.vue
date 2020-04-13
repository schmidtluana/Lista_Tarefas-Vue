<template>
  <div id="list">
      <div class="tarefas" v-for="(list, index) in tarefas" :key="index">
        {{list.texto}}
      </div>
  </div>
</template>

<script>
export default {
  name: "TodoList",
  props: ["tarefas"]
}
</script>

<style>
#list{
    width: 400px;
    height: 150px;
    border: 2px solid #ffffff;
    margin:50px auto 40px auto;
    display: flex;
    flex-wrap: wrap;
    overflow: auto;
}
.tarefas{
 height: 20px;
 width: tarefas ;
 text-align: center;
 border: darkcyan solid 2px;
 margin: 7px 5px -9px 7px
 
}
</style>