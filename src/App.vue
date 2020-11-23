<template>
  <div>
    {{todos}}
    <todos v-model="todos"></todos>
    <todos v-model="todos"></todos>
    <todos v-model="todos"></todos>
    <button @click="addTodo">Ajouter une tâche</button>
  </div>
</template>

<script>
import Todos from './components/Todos'

export default {
  data () {
    return {
      slides: 5,
      todos: [{
        name: 'Demo',
        completed: true
      }]
    }
  },
  methods: {
    addTodo () {
      this.todos.push({
        name: 'Jean',
        completed: false
      })
    },
    addSlide () {
      this.slides++
    },
    removeSlide () {
      this.slides--
    }
  },
  components: {
    Todos
  }
}
</script>

