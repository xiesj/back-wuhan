<template>
  <div>
    <div class="container">
      <div class="banner">
        <img src="/src/assets/banner.webp">
      </div>
      <div>
        <div class="article-content">
          <p style="text-align:center;line-height:2.9em;">
            <strong><span style="font-family:方正大标宋简体;font-size:1.2rem;">返汉申请结果查询</span></strong>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import {
    XHeader,
    Flexbox,
    FlexboxItem,
    XButton
  } from 'vux'
  export default {
    components: {
      XHeader,
      Flexbox,
      FlexboxItem,
      XButton
    },
    data() {
      return {}
    }
  }
</script>

<style>
  img {
    max-width: 100%;
  }
  .banner img{
    border-radius: 10px;
  }
  .action-bar {
    padding-top: 10px;
    padding-bottom: 10px;
  }
  .container {
    padding: 15px;
  }
  .article-content {
    color: #666;
  }
</style>
