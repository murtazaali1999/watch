<template>
<no-ssr placeholder='loading...'>
    <carousel-3d :height="280" :width="400" :border="1" :autoplay="true" :autoplay-timeout="2400">
        <slide v-for="(slide,i) in slides" :index="i" :key="i">
            <img v-bind:src="slide.src"/>
        </slide>
    </carousel-3d>
</no-ssr>
</template>
<script>
export default{
    data(){
        return{
            slides:[
                {src:require('../assets/1.jpg')},

                {src:require('../assets/2.jpg')},
                
                {src:require('../assets/3.jpg')},
                
                {src:require('../assets/4.jpg')},
                
                {src:require('../assets/5.jpg')},
            ]
        }
    }
}
</script>
<style>
.carousel-3d-slide{
    height: 100% !important;
}
</style>