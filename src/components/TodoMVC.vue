<template>
  <div>
    <input v-on:keyup.enter="addTask" v-model="newTask"/>
    <div v-for="task in tasks" v-if="all || task.completed=== statusToShow ">
      <input
        v-model="task.completed"
        type="checkbox"
        :id="task.name"
      />
      <label :for="task.name">{{task.name}}</label>
    </div>
    <button v-on:click="all=true">all</button>
    <button v-on:click="statusToShow=true; all=false">completed</button>
    <button v-on:click="statusToShow= false; all=false">active</button>
  </div>
</template>

<script>
export default {
  name: 'TodoMVC',
  data () {
    return {
      newTask: '',
      tasks: [],
      statusToShow: false,
      all: true
    }
  },

  methods: {
    addTask () {
      this.tasks.push({name: this.newTask, completed: false});
      this.newTask = '';
    },

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
