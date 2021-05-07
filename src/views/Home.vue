<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <hello-world msg="Welcome to Your Vue.js App"/>
    <hr>
    <AboutTest msg="About this information" @remove2="testRemove"></AboutTest>
    <AboutTest msg="About this information" @remove2="testRemove"></AboutTest>
    <AboutTest :msg="jin" @remove2="testRemove"></AboutTest>
    {{reverMsg}}
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import AboutTest from '@/components/AboutTest.vue'

export default {
  name: 'Home',
  components: {
    'hello-world':HelloWorld,
    AboutTest
  },

  data(){
    return {
      jin: 'jinlong'
    }
  },

  methods:{
    testRemove(){
      alert('点击了删除');
    }
  },
  computed:{
    reverMsg:function(){
      return this.jin.split('').reverse().join('');
    }
  }
}
</script>
