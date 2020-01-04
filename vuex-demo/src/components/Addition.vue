<template>
  <div>
    <!-- <h3>当前最新的count值为：{{$store.state.count}}</h3> -->
    <h3>{{$store.getters.showNum}}</h3>
    <button  @click="btnHandle1">+1</button>
    <button  @click="btnHandle2">+N</button>
    <button  @click="btnHandle3">+1 Async</button>
    <button  @click="btnHandle4">+N Async</button>
  </div>
</template>

<script>
export default {
  methods: {
    btnHandle1 () {
      this.$store.commit('add')
    },
    btnHandle2 () {
      this.$store.commit('addN', 3)
    },
    btnHandle3 () {
      this.$store.dispatch('addAsync')
    },
    btnHandle4 () {
      this.$store.dispatch('addNAsync', 5)
    }
  }
}
</script>

<style lang='less' scoped>

</style>
