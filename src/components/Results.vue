<template>
  <div>
    Reaction Time: {{score}} ms
   <p class="rank"> {{ rank }}</p>
  </div>
</template>

<script>
export default {
    props:['score'],
    data(){
        return{
            rank: null
        }
    },
    mounted(){
        if(this.score < 450){
            this.rank = 'Ninja Fingers'
        }else if(this.score < 800){
            this.rank = 'Rapid Reflexese'
        }
        else{
            this.rank = 'snail pace...'
        }
    }


}
</script>

<style>
.rank{
    font-size:1.4em;
    color: #0faf87;
    font-weight: bold;
    
}
</style>