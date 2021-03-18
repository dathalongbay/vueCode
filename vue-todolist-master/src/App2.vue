<template>
  <section>
    <div class="row justify-content-center mt-4">
      <input v-model="inputField" v-on:keyup.enter="addTodo" class="mr-1" placeholder="Todo Item" />
      <button @click="addTodo" class="btn btn-primary">Add Todo</button>
    </div>
  </section>

  <section>
    <input type="text" v-model="inputField" v-on:keyup.enter="addTodo"
    class="" placeholder="">

    <button @click="addTodo" @dblclick="" @keyup="" class="btn btn-success">
      Add todo
    </button>
  </section>
</template>

<script>
import test from './components/test';

export default {
  'name': 'App2',
  components: {
    // khai báo các components con
    test
  },
  data() {
    return {
      inputField: '',
      todoList: []
    }
  },
  methods: {
    addTodo: function(todo) {
      todo = this.inputField;
      this.todoList.push({name: todo, complete: false});
      this.inputField = '';
      console.log(this.todoList);
    },
  }
}
</script>
