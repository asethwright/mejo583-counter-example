<template>
  <div class="Test">
    <p @click="sayHello">Test {{ message }}</p>
  </div>
</template>

<script>
export default {

  data () {
    return {
      message: 'Here is my message'
    }
  },

  methods: {
    // sayHello: function () {
    // }
    sayHello () {
      this.message = 'changed message'
    }
  }
}
</script>

<style>
.Test {
}
</style>
