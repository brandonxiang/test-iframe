<template>
<div> 
  <div style="width:100%;height:1000px;background-color:#26a2ff;"></div>
<mt-navbar class="page-part" v-model="selected">
  <mt-tab-item id="1">选项一</mt-tab-item>
  <mt-tab-item id="2">选项二</mt-tab-item>
  <mt-tab-item id="3">选项三</mt-tab-item>
</mt-navbar>

<!-- tab-container -->
<mt-tab-container v-model="selected">
  <mt-tab-container-item id="1">
    <mt-cell v-for="n in 20" :title="'内容 ' + n" :key="n"></mt-cell>
  </mt-tab-container-item>
  <mt-tab-container-item id="2">
     <mt-cell v-for="n in 15" :title="'选项 ' + n" :key="n"></mt-cell>
  </mt-tab-container-item>
  <mt-tab-container-item id="3">
    <router-link v-for="n in 5" :key="n" to="detail">测试{{n}}</router-link>
  </mt-tab-container-item>

</mt-tab-container>
</div>
</template>

<script>
export default {
  data(){
    return {
      selected : "1"
    }
  }
}
</script>

<style>
html,body {
  margin:0;
  padding: 0;
}
</style>
