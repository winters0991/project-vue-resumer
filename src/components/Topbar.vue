<template>
  <div id="topbar">
    <div class='wrapper'>
      <span class='logo'>Resume</span>

      <div class='actions'>
        <button class="primary">保存</button>
        <button>预览</button>
      <div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Topbar'
}
</script>

<style scoped lang='scss'>
#topbar {
  background: #fff;
  box-shadow: 0 1px 3px 0 rgba(0,0,0,.25);

  > .wrapper {
    min-width: 1024px;
    max-width: 1440px;
    height: 64px;
    margin: 0 auto;
  }
  > .wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 16px;
  }
  .logo {
    font-size: 24px;
    color: #000;
  }
}
button {// 由于加了 scoped， 所以这个 button 选择器只在本组件内有效，不会影响其他组件
  width: 72px;
  height: 32px;
  border: none;
}
</style>
