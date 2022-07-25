<template>
    <figure>
      <img :src="item.image" :alt="item.name" />
      <figcaption>
        <dl>
          <dt></dt>
          <dd>{{item.name}}</dd>
          <p>{{item.price}}</p>
        </dl>
      </figcaption>
    </figure>
</template>


<script>
export default {
  props:{
        item:{type:Object}
    }
}
</script>

<style scoped>
/* #box02>#section{
  width: 95.83333333333333%;
  margin: 0 auto;
}
#box02>section{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around
} */

figure{
  width:22%;
  margin-bottom: 60px;
}
figure>img{
  margin-bottom: 20px;
}
figure>figcaption>dl>dt{
  margin-bottom: 20px;
  font-size: 15px;
  font-weight: bold;
}
figure>figcaption>dl>dd{
  margin-bottom: 20px;
}
figure>figcaption>dl>p{
  color: red;
}
</style>