<template>
  <div>
    <div class="container">
      <div class="banner">
        <img src="../assets/banner.png">
      </div>
      <div>
        <div class="article-content">
          <p style="text-align:center;line-height:2.9em;">
            <strong><span style="font-family:方正大标宋简体;font-size:1.2rem;">返汉申请结果查询</span></strong>
          </p>
          <div class="form">
            <div class="form-row">
              <div class="form-label">身份证号</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="card_id" placeholder="填写您的身份证号(必填)">
              </div>
            </div>
            <div class="form-row botton-box">
              <x-button type="primary" @click.native.stop="search">查询</x-button>
            </div>
          </div>
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
      return {
        card_id: ''
      }
    },
    methods: {
      submit() {
      }
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
    font-size: 14px;
  }
  .form-label {
    font-size: 14px;
    color: rgb(66,66,66);
    padding-top: 10px;
  }
  .form-input {
    box-shadow: inset 0 1px 1px rgba(0,0,0,.075);
    height: 36px;
    padding: 6px 8px;
    border: 1px solid #ccc;
    color: #555;
    background-color: #fff;
    font-size: 12px;
    width: 100%;
    border-color: rgb(240, 239, 239);
    box-sizing: border-box;
    transition: none;
  }
  .form-input:focus {
    outline: none;
    box-shadow: inset 0 1px 1px rgba(102,175,233,.3);
    border-color: rgba(102,175,233,.6);
  }
  .form-textarea {
    height: 100px;
    resize: none;
  }
  .form-radio {
    vertical-align: text-bottom;
    margin-bottom: 1px;
  }
  .form-label > .form-radio:first-child {
    margin-left: 20px;
  }
  .form-radio-label {
    padding-right: 10px;
  }
  .form-group-padding {
    padding-top: 7px;
  }
  .botton-box {
    padding-top: 20px;
    padding-bottom: 40px;
  }
  .file-delete {
    text-decoration: underline;
  }
</style>
