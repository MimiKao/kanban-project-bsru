<template>
  <div id="app">
   <Kanban :data="data"/>    
  </div>
</template>

<script>
import Kanban from "./components/Kanban"

export default {
  name: 'App',
  components: {
   Kanban
  },
  data(){
    return{
      data:[
        {
          name:"todo",
          color:"#FF9999",
          tasks:[]
        },
         {
          name:"doing",
          color:"#CC0033",
          tasks:[]
        },
         {
          name:"done",
          color:"#ebdd89",
          tasks:[]
        }
      ]
    }
  }
}
</script>

<style>
#app {
  height: 100vh;
}
</style>
