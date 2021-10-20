<template>
  <view class="container">
    <Statusbar />
    <Header title="ACT-APP"/>
  </view>
</template>

<script>
  import Statusbar from './components/Statusbar';
  import Header from './components/Header';

  export default {
    components: {
      Statusbar,
      Header
    }
  }
</script>

<style>
.container {
  background-color: white;
  flex: 1;
}
.statusbar {
  background-color: #FFCE00;
  height: 50px;
}
</style>
