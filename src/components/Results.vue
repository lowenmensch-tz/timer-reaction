 <template>
    <p>Reaction time: {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
 </template>
 
 <script>
 export default {
     props: ['score'],

     data(){
         return {
             rank: null,
         }
     },

     mounted(){
         if(this.score){
             this.rank = 'Ninja finger';
         } else if (this.rank < 400) {
            this.rank = 'Rapid Reflexes';
         } else {
            this.rank = 'Snail pace...';
         }
     }
 }
 </script>
 
 <style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
 </style>