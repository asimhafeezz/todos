<template>
  <div id="app">
    <Todos v-bind:todos="todos" />
  </div>
</template>

<script>
import Todos from './components/Todos'

export default {
  name: 'App',
  components: {
    Todos
  },
  data(){
    return{
      todos:[
        {
        task: "Task 1",
        due: "18 Jan 2021",
        complete: true
        },
        {
        task: "Task 2",
        due: "18 Jan 2021",
        complete: false
        },
        {
        task: "Task 3",
        due: "19 Jan 2021",
        complete: true
        },
        {
        task: "Task 4",
        due: "19 Jan 2021",
        complete: false
        }
      ]
    }
  }
}
</script>

<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  }

body{
  line-height: 1.4;
  }
</style>
