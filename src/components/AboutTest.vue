<template>
    <div id="divAbout">
        {{msg}}
        <br>
        <button @click="$emit('remove2')">删除删除</button> |
        <button @click="count++">点击了{{count}}次</button>  |
        {{rever2}}
    </div>

</template>

<script>
export default {
    name:'About',
    props:{
        msg:String
        // msg:{
        //     type:String,
        //     require:true
        //     }
    },    // props:['msg'] 这么写也可以

    data(){
        return {
            count:0,
            jin:'fangfang'
        }
    },

    emits:['remove2'],
    // emits:{
    //     remove2:()=>{
    //         return true;
    //     }
    // }

    computed:{
    rever2:function(){
      return this.jin.split('').reverse().join('');
    }
  }
}
</script>

<style scoped>
    div {
        background-color: bisque;
        border: 1px solid rgb(89, 148, 140);
        width: 100%;
        margin: auto;
        text-align: center;
        font-size: 32px;
    }
</style>