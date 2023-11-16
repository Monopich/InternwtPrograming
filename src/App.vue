<template>
  <div class="container">
    <Menu></Menu>
    <div class="Categories">
      <Categories
        v-for="i in Categories"
        :bg="i.bg"
        :ItemName="i.ItemName"
        :Img="i.Img"
        :Amount="i.Amount"
      ></Categories>
    </div>
    <div class="banner">
      <Banner
        v-for="i in Banner"
        :bannerBg="i.bannerBg"
        :Title="i.Title"
        :img="i.img"
        :btnColor="i.btnBg"
      ></Banner>
     
    </div>
    
  </div>
  <!-- http://127.0.0.1:5500/dist/index.html -->
</template>
<script>

import { mapState } from "pinia";
import {useProductStore} from "./store/ProductStore.js"
import Button from "./components/Button.vue";
import Categories from "./components/Categories.vue";
import Banner from "./components/Banner.vue";
import Menu from "./components/Menu.vue";
export default {
  name: "App",
  components: {
    Button,
    Categories,
    Banner,
    Menu,
  },
  computed: {
    ...mapState (useProductStore,["Categories"]),
    ...mapState (useProductStore,["Banner"]),

  },
};
</script>

<style>
.container{
  width: 100%;
  height: 100vh;
  display: flex; 
  flex-direction: column; 
  
}
.Categories{
  display: flex; 
  flex-direction: row;
  padding:20px;
}
.banner{
  margin-top: 40px;
  display: flex; 
  flex-direction: row; 
  margin-left:20px;

}

</style>