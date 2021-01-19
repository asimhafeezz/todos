<template>
    <div class="todos-container">
        <h1>Tasks</h1>
        <div v-for="todo in todos" :key="todo.task">
            <h3 class="todo" v-on:click="markComplete(todo)" v-bind:class="{'is-complete': todo.complete}">{{todo.task}}{{todo.due}}</h3>
        </div>
    </div>
</template>

<script>
export default {
    name:"Todos",
    props:["todos"],
    methods: {
        markComplete: function(todo) {
            console.log(todo.complete)
            todo.complete = !todo.complete
        }
    }
}
</script>


<style scoped>
.todos-container{
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    height: 100vh;
}

.todo{
    padding: 2rem;
    width: 300px;
    text-align: center;
    cursor: pointer;
    margin: .7rem 0;
}

h1{
    margin-bottom: 1rem;
}

.is-complete{
    background-color: rgb(50, 136, 50);
    text-decoration: line-through;
}
</style>


