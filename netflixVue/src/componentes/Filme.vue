<template>
     <div class="t-card" v-bind:style="efeitoClick" v-on:click="clickEfeito()" v-on:mouseout="removeClickEfeito()">
        <div class="t-card__media">
            <img class="t-card__img" v-bind:src="imagem" alt=""/>
        </div>
        <div class="t-card__details">
            <div class="t-card__title">
                {{ titulo }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['titulo', 'imagem'],
    data(){
        return{
            efeitoClick: null
        }
    },
    methods:{
        clickEfeito: function(){
            this.efeitoClick = 'transform: scale(1.9); margin-right: 110px'; //efeito para quando clicar no filme, ficar maior 
        },
        removeClickEfeito: function(){
            this.efeitoClick = null;
        }
    }
}
</script>

<style lang="scss">

</style>