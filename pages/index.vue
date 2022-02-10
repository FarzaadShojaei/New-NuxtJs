<template>
    <div>
       <div v-for="home in homes" :key="home.objectID" style="float:Left;margin:10px">
        <home-card-vue :home="home"></home-card-vue>
       </div>
    </div>
</template>
<script>
import homes from '../data/homes.json'
//import HomeCard from '../components/HomeCard.vue'
export default {
   // components:{
      //  HomeCard,
  //  },
  head(){
      return {
          title:'Homepage',
          meta:[{
              name:'description',
              content:'This is The Homepage',
              hid:'description'
          }]
      }
  },
    data(){
        return {
            homes:homes.slice(0,3)
        }
    }
}
</script>