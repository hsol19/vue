<template>
<div>
  <!-- (item,index in 배열의 이름) -->
    <figure v-for="(item,index) in products" :key="index">
      <img :src="item.image" :alt="item.name" />
      <figcaption>
        <dl>
          <dt>{{ite.title}}</dt>
          <dd>{{item.name}}</dd>
          <p>{{item.price}}</p>
        </dl>
      </figcaption>
    </figure>
</div>
</template>

<script>
import SubTwoData from '@/assets/data.json'
// import SubTwo from '@/components/SubTwo.vue'


export default {
  data(){
    return {
     products:SubTwoData 
    }
  } 
  // ,
  // created(){
  //   fetch('./assets/data.json')
  //   .then(response => response.json()
  //   .then(data =>this.products = data))
  // }
  ,
  components:{
    // SubTwo 
  },
  computed:{},
  methods:{}
}
</script>


<style scoped>
img{
  max-width: 100%;
}

div{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
</style>