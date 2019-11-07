<template>
  <div id="app" class="container">
    <mt-header fixed title="CMS"></mt-header>

    <router-view></router-view>

    <mt-tabbar v-model="selected">
      <mt-tab-item id="home">
        <router-link to="/"  tag="span">
          <i class="mui-icon mui-icon-home"></i> <br>
          
          主页
        </router-link>
      </mt-tab-item>
      <mt-tab-item id="member">
        <router-link to="/member"  tag="span">
          <i class="mui-icon mui-icon-contact"></i><br>
          会员
        </router-link>
      </mt-tab-item>
      <mt-tab-item id="cart">
        <router-link to="/cart"  tag="span">
          <i class="mui-icon mui-icon-extra mui-icon-extra-cart">
            <i class="mui-badge">0</i>  
          </i><br>
          购物车
        </router-link>
      </mt-tab-item>
      <mt-tab-item id="search">
        <router-link to="/search"  tag="span">
          <i class="mui-icon mui-icon-search"></i><br>
          搜索
        </router-link>
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>

<script>
export default {
  data:function(){
    return  {
      selected:""
    }
  }
}
</script>


<style lang="less">
  .container{
    padding-top: 40px;
    padding-bottom: 40px;
    overflow: hidden;
  }

  //.mint-tab-item默认的文字颜色
  .mint-tab-item {
    color: gray;
  }

  .mui-icon{
    margin-bottom: 3px;
  }

  .mui-icon-extra-cart{
    position: relative;

    .mui-badge{
      position: absolute;
      right: -5px;
      top: -5px;
    }
  }


</style>
