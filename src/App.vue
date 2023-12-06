<template>
  <div class="main">
  <carousel :itemsToShow="1.5">
    <slide v-for="(list, index) in lists" :key="index">
      <img :src="require(`/Users/eraorynbaigmail.com/Desktop/assignment13/part3/src/assets/${list.photo}`)" alt="Slide" />
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
</div>
</template>

<script>
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';



export default {
  name: 'App',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data() {
    return {
      lists: [
        { photo: 'ron6.png' },
        { photo: 'ron7.png' },
        { photo: 'ron8.png' },
        { photo: 'ron9.png' },
        { photo: 'ron10.png' },
      ],
    };
  },
};
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
.main{
 padding:120px 100px;
 background-color: rgb(38, 40, 165);
}

img {
  width: 300px;
  height: 300px;
  border-radius:10%;
  outline: none;
  border: none;
}
</style>