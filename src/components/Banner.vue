<template>
    <div class="banner-box" :style="{ backgroundColor: bannerBg }">
      <div>
        <p class="text">{{ Title }}</p>
        <Button class="btn" :btnBg="btnColor"></Button>
      </div>
      <img class="image" :src="img" alt="" />
    </div>
  </template>

  
  <style scoped>
  @import url("https://fonts.googleapis.com/css2?family=Josefin+Sans&family=Lato:ital,wght@0,300;0,400;1,300&family=Quicksand:wght@300;400;700&display=swap");
  
  .banner-box {
    width: 480px;
    height: 300px;
    display: flex;
    position: relative;
    align-items: center;
    background-color: rgba(182, 182, 182, 1);
    border-radius: 10px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    /* border: 1px solid #81B13D; */
    margin-right: 17px;
  }
  .text {
    left: 48px;
    top: 75px;
    width: 271px;
    height: 48px;
    position: absolute;
    font-family: Quicksand;
    font-weight: 700;
    font-size: 24px;
  }
  .btn {
    top: 240px;
    left: 48px;
    position: absolute;
    border: none;
    border-radius: 3px;
  }
  .image {
    width: 411px;
    height: 181px;
    margin-top: 95px;
    margin-left: 50px;
  }
  </style>

<script>
import Button from "./Button.vue";
export default {
  name: "Banner",
  components: {
    Button,
  },
  props: {
    bannerBg: String,
    img: String,
    Title: String,
    btnColor: String
  },
  
};
</script>
  