<template>
  <div class="v-main-wrapper">
    <v-catalog />
    <v-cart />
  </div>
</template>
<script>
  import vCatalog from './v-catalog';
  import vCart from './v-cart'
  export default {
    components: { vCatalog , vCart},
    name: "v-main-wrapper",
    data(){
      return{
        title: 'Main wrapper'
      }
    },


  }
</script>
<style>
  .v-main-wrapper{
    max-width: 900px;
    margin: 0 auto;
  }
</style>