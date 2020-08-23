<template>
  <div>
    <h3>当前最新的count值为：{{ $store.state.count }}</h3>
    <h2>{{ $store.getters.showNum }}</h2>
    <button @click="btnHandler1">+1</button>
    <button @click="btnHandler2">+N</button>
    <button @click="btnHandler3">+1 Async</button>
    <button @click="btnHandler4">+N Async</button>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {
    btnHandler1() {
      this.$store.commit('add')
    },
    btnHandler2() {
      this.$store.commit('add', 5)
    },
    btnHandler3() {
      this.$store.dispatch('addAsync')
    },
    btnHandler4() {
      this.$store.dispatch('addNAsync', 5)
    }
  }
}
</script>
