<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="div1">
      <div class="div2">宋</div>
      <p>义信</p>
    </div>
    <div class="div3">属性嵌套</div>
    <div class="div4">继承</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    $color:red;
    .hello{
      color:$color;
      .div1{
        color:blue;
        &:hover{/**&代表.div1 */
          color:purple
        } 
        .div2{
          color:green;
        }
      }
    }
    h1:hover{
      color:purple
    }
    /**属性嵌套 */
    .div3{
      border:{
        style:solid;
        width:5px;
        color:blue;
      }
    }
    /**继承 */
    .div4{
      @extend .div3;
      border-width:2px;
      border-radius:1rem;
    }
</style>