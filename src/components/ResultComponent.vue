<template>
    <div class="result">
        <p>Reaction time - {{ score }} ms</p>
        <p class="rank"> {{ rank }}</p>
    </div>
</template>

<script>
export default {
    props: ['score'],
    //check scores
    data () {
        return {
            rank:null
        }
    },
    mounted() {
        if(this.score < 250){
            this.rank = 'Ninja Fingers!'
        } else if(this.score < 400){
            this.rank = 'Rapid Reflexex'
        }else{
            this.rank = 'Snail pace'
        }
    }
}
</script>
<style>
    .rank{
        font-size: 1.43em;
        color:#0faf87;
        font-weight: bold;
    }
</style>