<template>
  <div id="app">
   <Kanban :data="data" :create_task_submit="create_task_submit"/>    
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
          tasks:[{
            task_name: "test"
          }]
        },
         {
          name:"doing",
          color:"#CC0033",
          tasks:[{
            task_name: "test"
          }]
        },
         {
          name:"done",
          color:"#ebdd89",
          tasks:[{
            task_name: "test"
          }]
        }
      ]
    }
  },
  methods:{
    create_task_submit(column_index,item){
      this.data[column_index].tasks.push(item)
    }
  }
}
</script>

<style>
#app {
  height: 100vh;
}
</style>
