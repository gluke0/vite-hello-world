<!-- JS -->
<script>
export default {
    data() {
        return{
            image: 'jumbotron.png'
        }
    },
    methods: {
        getImagePath: function (imgPath){
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<!-- HTML -->
<template>
    <div id="jumbotron">
        <img :src="getImagePath(`../assets/${image}`)" alt="jumbotron vite">
    </div>
</template>

<!-- CSS -->
<style scoped>
#jumbotron {
    margin: auto;
    width: 50%;
}
img{
    width: 100%;
}
</style>
