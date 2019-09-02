<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div @click="handleCountClick">点击次数：{{count}}</div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  data () {
    return {
      count: 0
    }
  },
  methods: {
    handleCountClick () {
      this.count++
      localStorage.count = this.this.count
    }
  },
  async mounted () {
    this.count = Number(localStorage.count) || 0
  }
}
</script>
