<template >
  <div class="header mt-3">
    <div class="header-contain p-3 d-flex w-100 justify-content-around">
      <div class="left d-flex gap-3">
        <div
          class="left-shop d-flex gap-3 align-items-center justify-content-center"
        >
          <span>سبد خرید</span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-cart"
            viewBox="0 0 16 16"
          >
            <path
              d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .491.592l-1.5 8A.5.5 0 0 1 13 12H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5M3.102 4l1.313 7h8.17l1.313-7zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4m7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4m-7 1a1 1 0 1 1 0 2 1 1 0 0 1 0-2m7 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2"
            />
          </svg>
        </div>
        <div
          class="left-account d-flex gap-2 align-items-center justify-content-center"
        >
          <span>حساب کاربری</span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            fill="currentColor"
            class="bi bi-person"
            viewBox="0 0 16 16"
          >
            <path
              d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6m2-3a2 2 0 1 1-4 0 2 2 0 0 1 4 0m4 8c0 1-1 1-1 1H3s-1 0-1-1 1-4 6-4 6 3 6 4m-1-.004c-.001-.246-.154-.986-.832-1.664C11.516 10.68 10.289 10 8 10s-3.516.68-4.168 1.332c-.678.678-.83 1.418-.832 1.664z"
            />
          </svg>
        </div>
      </div>
      <div class="center">
        <div class="search d-flex border rounded-4 align-items-center">
          <div class="search-icon p-2">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="22"
              height="22"
              fill="#A72F3B"
              class="bi bi-search text-danger"
              viewBox="0 0 14 14"
            >
              <path
                d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001q.044.06.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1 1 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0"
              />
            </svg>
          </div>
          <input type="text " placeholder="" class="border-0 w-100 text-end" />
          <span class="placeholder bg-white stick pe-3"> استیکر </span>
        </div>
      </div>
      <div class="right">
        <img src="../assets/image/Frame 26088044.png" alt="" />
      </div>
    </div>
  </div>
  <div class="category w-100 mt-5 d-flex flex-column align-items-center">
    <div class="category-head d-flex w-75">
      <p>جشن و مهمانی</p>
      <p>کارت و پوستر</p>
      <p>مدرسه و اداره</p>

      <p>اکسسوری</p>
      <p>قاب موبایل</p>

      <p>لوازم خانه</p>

      <p>پوشاک</p>
    </div>
  </div>
  <div class="Card d-flex justify-content-center row">
    <div class="Card-contain d-flex flex-column col-9">
      <div class="Card d-flex flex-column justify-content-center w-100">
    <div class="filter-item d-flex w-100 mt-3">
      <div class="d-flex item w-100 justify-content-end">
        <p>ارزان ترین</p>
        <p>گران ترین</p>

        <p>پرفروش ترین</p>
        <p>جدید ترین</p>
        <div class="line d-flex flex-column gap-2">
          <span class="full">پربازدید ترین</span>
          <span class="line-down"></span>
        </div>
      </div>
    </div>
    <div class="Card-contain d-flex flex-column justify-content-center">
      <div class="cardItems d-flex justify-content-end row">
        <div
          class="cardItem border rounded-4 col-3"
          v-for="(item, index) in usebook.allProduct" :key="index">
          <cardItem :priceProduct='priceProduct' :nameProduct="nameProduct" :index="index"/>
        </div>
      </div>
    </div>
  </div>
      
  
    </div>
    <div class="filter border rounded-3 ms-3 col-3 mt-5">
      <div
        class="filter-contain d-flex flex-column align-items-center gap-4 p-3"
      >
        <div class="title d-flex justify-content-between w-100 p-2">
          <span class="delete text-danger fw-bold">حذف فیلتر ها </span>
          <span class="">فیلتر ها </span>
        </div>
        <div class="design d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon w-25 border d-flex">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="12"
                height="12"
                fill="currentColor"
                class="bi bi-caret-down-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                />
              </svg>
            </div>
            <span class="w-75 text-end w-75 text-secondary">نوع طرح</span>
          </div>
          <div class="line"></div>
        </div>
        <div class="distance d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon w-25">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="14"
                height="14"
                fill="currentColor"
                class="bi bi-caret-down-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                />
              </svg>
            </div>
            <span class="text-end w-75 text-secondary">اندازه</span>
          </div>
          <div class="line"></div>
        </div>
        <div class="color d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon w-25">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="14"
                height="14"
                fill="currentColor"
                class="bi bi-caret-down-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                />
              </svg>
            </div>
            <span class="text-end w-75 text-secondary">رنگ</span>
          </div>
          <div class="line"></div>
        </div>
        <div class="delivary d-flex flex-column align-items-center w-100">
          <div class="up w-100">
            <div class="icon-check d-flex w-100 justify-content-between">
              <div
                class="form-check w-100 form-switch d-flex justify-content-between"
              >
                <input
                  class="form-check-input"
                  type="checkbox"
                  role="switch"
                  id="flexSwitchCheckDefault"
                />
                <label
                  class="form-check-label text-secondary"
                  for="flexSwitchCheckDefault"
                  >ارسال امروز</label
                >
              </div>
            </div>
          </div>
          <div class="line"></div>
        </div>
        <div class="available d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon-check d-flex w-100">
              <div
                class="form-check form-switch w-100 d-flex justify-content-between"
              >
                <input
                  class="form-check-input"
                  type="checkbox"
                  role="switch"
                  id="flexSwitchCheckDefault"
                />
                <label
                  class="form-check-label text-secondary"
                  for="flexSwitchCheckDefault"
                  >فقط کالا های موجود</label
                >
              </div>
            </div>
          </div>
          <div class="line"></div>
        </div>

        <div class="graphic d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon-check d-flex w-100">
              <div
                class="form-check form-switch w-100 d-flex justify-content-between"
              >
                <input
                  class="form-check-input"
                  type="checkbox"
                  role="switch"
                  id="flexSwitchCheckDefault"
                />
                <label
                  class="form-check-label text-secondary text-end"
                  for="flexSwitchCheckDefault"
                  >فقط محصولات گرافیکی</label
                >
              </div>
            </div>
          </div>
          <div class="line"></div>
        </div>
        <div class="price d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon w-25">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="14"
                height="14"
                fill="currentColor"
                class="bi bi-caret-down-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                />
              </svg>
            </div>
            <span class="text-end w-75 text-secondary">محدوده قیمت</span>
          </div>
          <div class="line"></div>
        </div>
      </div>
    </div>
  </div>
  <div class="navigation w-75 mt-4 d-flex justify-content-center gap-3 align-items-center">
    <div
      class="next rounded-5 d-flex justify-content-center align-items-center"
    >
    <i class="bi bi-arrow-left left" id="left" @click="increase"></i>
    </div>
    <div
      class="navigation-contain d-flex border p-1 justify-content-center gap-4 rounded-5"
    >
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
        50
      </div>
      <div class="">. . .</div>
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
        10
      </div>
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
        9
      </div>
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
        8
      </div>
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
        7
      </div>
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
        6
      </div>

      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
        5
      </div>
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
        4
      </div>
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
       3
      </div>
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
    2
      </div>
      <div
        class="circle border border-black rounded-5 d-flex justify-content-center align-items-center"
      >
       1
      </div>
    </div>
    <div class="per rounded-5 d-flex justify-content-center align-items-center">
     
      <i class="bi bi-arrow-right right" @click="decrease" id="amir" ></i>
    </div>
  </div>
  <div class="footer_up p-5 w-100 d-flex justify-content-center mt-3">
    <div class="footer_up-contain d-flex w-100 px-5">
      <div class="left w-50 d-flex flex-column">
        <p class="text-white">ما را در شبکه های اجتماعی دنبال کنید</p>
        <div class="icon fs-4 d-flex gap-5">
          <i class="bi bi-instagram"></i>
          <i class="bi bi-facebook"></i>
          <i class="bi bi-pinterest"></i>
          <i class="bi bi-youtube"></i>
        </div>
      </div>
      <div class="right w-75 d-flex flex-column align-items-end gap-1">
        <span class="text fw-normal text-white">
          برای دریافت آخرین اخبار و تخفیف های جدید، ایمیل خود را واردنمایید
        </span>
        <div class="d-flex gap-2">
          <button
            type="button"
            class="button border-0 rounded-3 text-white bg-red"
          >
            ثبت
          </button>
          <input
            type="email"
            class="email border border-white text-white rounded-2 text-end"
            placeholder="ایمیل شما "
          />
        </div>
      </div>
    </div>
  </div>
  

  <div class="footer_down w-100 d-flex justify-content-center">
    <div class="footer_down-contain mt-5 d-flex w-100 px-5 justify-content-center gap-4">
      <div class="shop w-50">
        <div class="shop-contain d-flex flex-column w-100 h-100">
          <span
            class="overflow-hidden w-100 fw-bold text-white text-center title"
          >
            فروشگاه اینترنتی کاستومی
          </span>
          <div class="info w-100 gap-5 d-flex justify-content-center">
            <div class="d-flex">
              <span class="">پاسخگویی 24 ساعته 7 روز هفته</span>
            </div>
            <div class="d-flex gap-2 justify-content-end">
              <span class=""> 021-3456000 </span>
              <span class="">: تماس با پشتیبانی </span>
            </div>
          </div>
          <div class="image d-flex gap-3 justify-content-center">
            <img src="../../public/image/01.jpg" alt="" class="image" />
            <img src="../../public/image/02.jpg" alt="" class="image" />
            <img src="../../public/image/03.jpg" alt="" class="image" />
          </div>
        </div>
      </div>
      <div class="guid w-25 d-flex flex-column align-items-end gap-4">
        <div class="buy d-flex flex-column align-items-center">
          <span class="text-white">راهنمای خرید</span>
          <div class="line"></div>
        </div>
        <div class="d-flex flex-column align-items-end gap-3">
          <span class="text">راهنمای ثبت سفارش</span>
          <span class="text"> شیوه های پرداخت</span>
          <span class="text"> نحوه ارسال سفارش ها </span>
          <span class="text"> شرایط بازگرداندن محصول</span>
        </div>
      </div>
      <div class="several w-25 d-flex flex-column gap-3 align-items-end gap-4">
        <div class="buy d-flex flex-column align-items-center">
          <span>خدمات مشتریان</span>
          <div class="line"></div>
        </div>
        <div class="d-flex flex-column align-items-end gap-3">
          <span class="text">سوالات متداول</span>
          <span class="text"> حریم خصوصی</span>
          <span class="text"> ثبت شکایت </span>
          <span class="text"> ضمانت نامه محصولات </span>
        </div>
      </div>
      <div class="with w-25 d-flex flex-column align-items-end gap-4">
        <div class="buy d-flex flex-column align-items-center">
          <span>همراه با کاستومی</span>
          <div class="line"></div>
        </div>
        <div class="d-flex flex-column align-items-end gap-3">
          <span class="text"> فروش محصولات </span>
          <span class="text"> فرصت همکاری </span>
          <span class="text"> تماس با ما </span>
          <span class="text"> نقشه سایت </span>
        </div>
      </div>
    </div>
  </div>


</template>

<script setup>
import { onMounted,ref, watch } from 'vue';
import cardItem from './cardItem.vue';
import { useDetailStore } from '../stores/counter.js';

let priceProduct = ref([])
let nameProduct = ref([])
const usebook = useDetailStore();
onMounted(()=>{
 usebook.getname()

  
  
    

 watch(()=>usebook.allProduct,()=>{
  for(var i =0 ; i<20 ; i++){   
    nameProduct.value.push(usebook.allProduct[i]['attributes']['name'])
    priceProduct.value.push(usebook.allProduct[i]['attributes']['price'])
  }
 })
})
function decrease(){
    if( usebook.count>0){
      usebook.count-=1 

    }else{ 
      usebook.count=0
    }


   }
   function increase(){
    usebook.count+=1    
  }

;

</script>





<style scoped>
@import "../assets/product.css";
</style>

