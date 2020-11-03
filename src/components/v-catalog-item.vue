<template>
    <div class="v-catalog-item">
<img class="v-catalog-item__image" :src= "require('../assets/images/' + product_data.image) " alt="img">
        <p class="v-catalog-item__name">{{product_data.name}}</p>
        <p class="v-catalog-item__price">{{product_data.price}} тг. </p>
        <btn class="v-catalog-item__add-to-catr btn"
             @click="sendDataToPerent">Add to cart</btn>
    </div>
</template>

<script>
    export default {
        name: 'v-catalog-item',
        props:{
            product_data:{
                type: Object,
                default(){
                    return{}
                }
            }
        },
        methods:{
            sendDataToPerent(){
                this.$emit('sendArticle', this.product_data.article)
            }
        }
    }
</script>
<style lang="scss">
    .v-catalog-item{
        flex-basis: 25%;
        width: 20px;
        box-shadow: 0 0 8px 0 #c0e0e0;
        padding: 18px;
        margin-bottom: 18px;
&__image{
width: 100px;}
}
</style>