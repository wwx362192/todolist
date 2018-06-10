<template>
  <div>
      <input v-model="inputValue" type="text">
      <button @click="handerClick">提交按钮</button>
     
      <todo-item 
        v-for="(item , index) of lists"
        :key="index"
        :content="item"
        :index="index"
        @del="handerDel"
      ></todo-item>
  </div>
</template>

<script>
import todoitem from './components/todoitem'
export default {
  components:{
    'todo-item':todoitem
  },
  data(){
    return{
        inputValue: "",
        lists: []
      }
  },
  methods:{
    handerClick(){
      this.lists.push(this.inputValue);
      this.inputValue="";
    },
    handerDel(index){
      this.lists.splice(index,1);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
