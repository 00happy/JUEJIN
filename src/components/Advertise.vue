<template>
  <div class="ad">
    <i class="el-icon-close" @click="closeAd"></i>
    <img
      :src="imgSrc"
      alt=""
    />
    <el-button size="mini" class="adBtn">广告</el-button>
    <el-button size="mini" class="adBtn2">投放 广告</el-button>
  </div>
</template>

<script>
export default {
  props:{
    imgSrc:String
  },
  methods:{
    closeAd(e){
      e.target.parentElement.style = "display:none"
    },
  }
};
</script>

<style lang="scss" scoped>
.ad {
  cursor: pointer;
  position: relative;
  img {
    width: 100%;
    height: 200px;
  }
  .el-icon-close {
    position: absolute;
    top: 5px;
    right: 5px;
    display: none;
    color: grey;
  }

  .adBtn,
  .adBtn2 {
    position: absolute;
    bottom: 10px;
    right: 0px;
    font-size: 18px;
    transform: scale(0.6);
    color: #fff;
    background-color: rgba(0, 0, 0, 0.2);
  }
  .adBtn2 {
    right: -8px;
  }
  .adBtn2 {
    display: none;
  }
  .adBtn:hover {
    display: none;
  }
  .adBtn:hover + .adBtn2 {
    display: block;
  }
}
.ad:hover {
  .el-icon-close {
    display: block;
  }
}
</style>