<template>
  <div >
  <div class="image">
    <img alt="" :src="getImageUrl(arrimage[index])" class="img img-fluid" />
    
  </div>
  <div class="sticker mt-2 d-flex justify-content-end">
    <div
      class="text d-flex flex-column gap-1 name w-100 align-items-end"
    >
      <div class="d-flex justify-content-between w-100 border">
        <i class="bi bi-heart heart"></i>
        <h3 class="fs-5 overflow-hidden text-start">
          {{ props.nameProduct[index]}}
        </h3>
      </div>

      <p class="">قابل چاپ با اندازه دلخواه</p>
    </div>
  </div>
  <div class="price d-flex gap-2 p-3">
    <span class="fw-bold">{{ props.priceProduct [index] }}</span>
  </div>
  </div>
</template>

<script setup>
const props = defineProps({
  nameProduct: Array, 
  priceProduct : Array, 
  index:Number
  
})
import { useDetailStore } from "../stores/counter.js";
import { onMounted, ref, watch, watchEffect } from "vue";
onMounted(() => {
  loadData()

  
  usebook.getname()

})


const usebook = useDetailStore();
const loadData = async ()=>{
  await usebook.getname()
} 

const arrimage = ref([
  "1.jpg",
  "2.jpg",
  "3.jpg",
  "5.jpg",
  "6.jpg",
  "7.jpg",
  "8.jpg",
  "9.jpg",
  "4.jpg",
  "1.jpg",
  "2.jpg",
  "3.jpg",
  "5.jpg",
  "6.jpg",
  "7.jpg",
  "8.jpg",
  "9.jpg",
  "4.jpg",
  "1.jpg",
  "2.jpg",
]);
const getImageUrl = (imageName) => {
  return new URL(`../assets/image/${imageName}`, import.meta.url).href;
};
</script>

<style>

</style>
