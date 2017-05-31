<template>
  <div class='page'>
    <header>
      <Topbar/>
    </header>
    <main>
      <ResumeEditor/>
      <ResumePreview/>
    </main>
  </div>
</template>

<script>

import 'normalize.css/normalize.css'
import './assets/reset.css'

import Topbar from './components/Topbar'
import ResumeEditor from './components/ResumeEditor'
import ResumePreview from './components/ResumePreview'
import icons from './assets/icons'

export default {
  name: 'app',
  data: function(){
    return {
      text: '你好'
    }
  },
  components: {Topbar, ResumeEditor, ResumePreview},
  created(){
    document.body.insertAdjacentHTML('afterbegin', icons) //插入元素内部的第一个子节点之前
  }
}
</script>

<style lang='scss'>
  .page {
    height: 100vh;
    display: flex;
    flex-direction: column;
    background: #EAEBEC;

    >main {
      flex-grow: 1;
    }
    >main {
      min-width: 1024px;
      max-width: 1440px;
      margin-top: 16px;
      margin-bottom: 16px;
      display: flex;
      justify-content: space-between;
      align-self: center;
      width: 100%;
      padding: 0 16px;
    }
  }

#resumeEditor {
  width: 35%;
}
#resumePreview {
  width: 61.66667%;
  flex-grow: 1;
  margin-left: 16px;
}
svg.icon {
  height: 1em;
  width: 1em;
  fill: currentColor;
  font-size: 16px;
  vertical-align: -0.1em;
}

</style>
