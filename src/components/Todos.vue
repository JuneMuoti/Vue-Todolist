<template>
    <div>
        <div v-for="todo in todos" v-bind:key="todo.id">
            <Todoitem v-bind:todo="todo" v-on:del-todo="$emit('del-todo',todo.id)" />
        </div>
    </div>
</template>
<script>
import Todoitem from './Todoitem.vue';
export default {
    name:"Todos",
    components:{
        Todoitem
    },
    props:["todos"]
}
</script>


<style scoped>
h1{
    display: inline;
   color: aqua;
   margin-left: 50px;
}
</style>