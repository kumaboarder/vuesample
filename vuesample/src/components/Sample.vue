<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <span v-if="seen">Now you see me</span>
  <ol>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>
  </ol>
  <button v-on:click="reverseMessage">Reverse Message</button>
  <router-link to="/hello">Go to hello</router-link>
  </div>
</template>

<script>
export default {
  name: 'Sample',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      seen: true,
      todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue' },
      { text: 'Build something awesome' }
    ]
    }
  },methods: {
    reverseMessage: function () {
      this.msg = this.msg.split('').reverse().join('')
    }
  }
}
</script>
