<template>
    <p>Reaction time - {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ["score"],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 2500){
            this.rank = "ninja Fingers"
        } else if (this.score <4000 ){
            this.rank = "Rapid Reflexes"
        } else this.rank = "Snail pace..."
    }
}

// mounted: mounted hook -> this fires as soon as the component is mounted to the dom 
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>