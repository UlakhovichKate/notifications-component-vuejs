<template>
  <div class="container">
    <img alt="Vue logo" src="./assets/logo.png">
    <div class="row w-50 m-auto">
      <Message v-for="(alert, index) in alerts" :info=alert :key=index />
    </div>
  </div>
</template>

<script>
import Message from './components/Message.vue'

export default {
  name: 'App',
  components: {
    Message
  },
  data() {
    return {
      alerts: [
          {
            type: 'warning',
            msg: '!',
          },
          {
            type: 'success',
            msg: '^___^'
          },
          {
            type: 'danger',
            msg: ':`-('
          }
        ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
