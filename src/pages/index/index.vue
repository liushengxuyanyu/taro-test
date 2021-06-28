<template>
  <view class="index">
    <text @tap="goMine">{{ msg }}</text>
  </view>
</template>

<script>
import Taro from '@tarojs/taro'
import { ref } from 'vue'
import './index.css'

export default {
  setup() {
    const msg = ref('Hello world')
    return {
      msg
    }
  },
  methods: {
    goMine() {
      Taro.navigateTo({
        url: `../mine/index?t=${Date.now}`
      })
    }
  }
}
</script>
