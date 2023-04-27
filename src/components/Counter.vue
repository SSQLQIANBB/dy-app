<template>
  <view class="title">
    hello dyApp
  </view>
</template>

<script>
import { useCounterStore } from '../stores/counter'

export default {
  setup() {
    const counter = useCounterStore()

    const onAdd = () => {
      counter.count++

      // with autocompletion ✨
      // counter.$patch({count: counter.count + 1})

      // or using an action instead
      // counter.increment()
    }

    return {
      counter,
      onAdd
    }
  }
}
</script>

<style>
.title {
  font-size: 32px;
  text-align: center;
  background: skyblue;
}
</style>
