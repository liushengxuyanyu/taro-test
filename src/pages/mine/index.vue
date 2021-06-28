<template>
  <view class="mine">
    <text>{{ msg }}</text>
  </view>
</template>

<script>
import Taro from '@tarojs/taro'
import { ref } from 'vue'
import './index.css'

export default {
  setup() {
    const msg = ref('我是mine')
    return {
      msg
    }
  },
  onShow() {
    console.log('--- onshow ---')
  },
  onLoad(options) {
    console.log('onload: ', options)
  },
  beforeUnmount() {
    console.log('---- beforeUnmount ----')
  },
  methods: {}
}
</script>
