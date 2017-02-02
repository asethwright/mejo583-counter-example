<template>
  <div id="app">
    <button @click="clear">Clear</button>
    <h1>{{ total }}</h1>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add" v-if="showing"></Counter>
    <button @click="showing = true">Add It</button>
    <button @click="showing = false">Remove It</button>
  </div>
</template>

<script>
import Counter from './components/Counter'

// this.$evt.$emit (dispatch custom event)
// this.$evt.$on (add event listener)
// this.$evt.$off (remove event listener)

export default {
  name: 'app',
  components: {
    Counter
  },
  data () {
    return {
      total: 0,
      showing: false
    }
  },
  methods: {
    add () {
      this.total++
    },

    clear () {
      this.total = 0
      this.$evt.$emit('clear')
    }
  }
}
</script>

<style>
#app {
}
</style>
