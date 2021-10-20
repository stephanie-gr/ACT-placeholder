<template>
  <view class="header">
    <text class="title">{{ title }}</text>
  </view>
</template>

<script>
  export default {
    props: ['title']
  }
</script>

<style>
  .header {
    height: 60px;
    background-color:aquamarine;
    justify-content: center;
    align-items: center;
  }
  .title {
    color: black;
    font-weight: 900;
    
  }
</style>
