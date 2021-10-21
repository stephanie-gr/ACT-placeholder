<template>
  <view class="container">
    <Statusbar />
    <Header title="ACT-APP"/>
  <view class="inputContainer">
    <text-input class="input" v-model="newTodoText" />
    <touchable-opacity class="add-btn" :on-press="newTodo">
      <text class="btn-text">ADD</text>
    </touchable-opacity>
  </view>

  <view class="dropzone">
    <view 
      class="todo" 
      v-for="todo in todos" 
      :key="todo.id" 
    >
      <text>{{ todo.title }}</text>
    </view>
  </view>

  <!-- <ScrollTest /> -->
  </view>

</template>

<script>
  import Statusbar from './components/Statusbar';
  import Header from './components/Header';
  // import ScrollView from './components/ScrollTest';
  // import ScrollTest from './components/ScrollTest.vue';

  export default {
    data () {
      return {
        newTodoText: '',
        todos: [
          {
            id: 0,
            title: 'Go Shopping',
            done: false
          },
          {
            id: 1,
            title: 'Eat Food',
            done: false
          }
        ]
      }
    },
    components: {
      Statusbar,
      Header,
      // ScrollTest
    },
    methods: {
      newTodo () {
        this.todos.push({id: this.todos.length + 1, title: this.newTodoText})
      }
    }
  }
</script>

<style>
.container {
  background-color: white;
  flex: 1;
}
.inputContainer {
  flex-direction: row;
  justify-content: center;
  align-items: stretch;
  width: 100%;
}
.input {
  flex: 1;
  height: 35px;
  background-color: #F3F3F3;
  color: #888888;
}
.add-btn {
  width: 100px;
  height: 35px;
  justify-content: center;
  align-items: center;
  background-color: #FFCE00;
}
.btn-text {
  font-size: 18px;
  font-weight: 700;
}
.dropzone {
  background-color:lightpink;
  /* height: 50%; */
  margin-bottom: 10px;
  padding: 10px;
}
.todo {
  background-color: lightcyan;
  /* height: 30px; */
  margin-bottom: 10px;
  padding: 5px;
}

</style>
