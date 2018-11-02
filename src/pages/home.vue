<template>
    <div class="home">
        <div class="warp-banner" ref="homePage">
            <div class="logo">
                <h2>shouye</h2>
                <h4>Love to learn to love life</h4>
            </div>
        </div>
        <div class="menu">
            <h3>
                Javascript
            </h3>
            <div class="title-box">

            </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
      return {
        clientHeight:'',
      }
    },
    mounted(){
      // 获取浏览器可视区域高度
      this.clientHeight =   `${document.documentElement.clientHeight}`          //document.body.clientWidth;
      //console.log(self.clientHeight);
      window.onresize = function temp() {
        this.clientHeight = `${document.documentElement.clientHeight}`;
      };
    },
    watch: {
      // 如果 `clientHeight` 发生改变，这个函数就会运行
      clientHeight: function () {
        this.changeFixed(this.clientHeight)
      }
    },
    methods:{
      changeFixed(clientHeight){                        //动态修改样式
        console.log(clientHeight);
        this.$refs.homePage.style.height = clientHeight+'px';
      },
    }
}
</script>

<style scoped>
    *{
        color: #fff;
    }
    .home{
        width: 100%;
        height: 100%;
    }
    .warp-banner{
        position: relative;
        align-content: center;
        width: 100%;
        height: 100%;
    }
    .warp-banner .logo{
        height: 100%;
        position: absolute;
        z-index: 99;
        font-family: Teko,sans-serif;
        text-shadow: 8px 8px #000;
        text-transform: uppercase;
    }
    .warp-banner .logo h2{
        font-size: 50px; 
        margin-bottom: 10px;
    }
    .warp-banner .logo h4{
        font-size: 30px; 
    }
    .menu{
        height: 1000px;
        background: #34393f;
        text-align: center;
    }
    .menu h3{
        margin: 0 auto;
        width: 30%;
        text-align: left;
        line-height: 40px;
        padding-top: 10px; 
    }
    .title-box{
        width: 30%;
        height: 300px;
        margin: 10px auto;
        background: #292929;
        border-radius: 3px;
        box-shadow: 2px 6px 17px rgba(0,0,0,.39);
    }
</style>

