<template>
  <div class="work">
    <h1>송기영의 Vue 실습 페이지</h1>
  </div>
  <hr />
  <TeamComponent name="송기영" food="마라탕" teamNum="1" srcUrl="../../public/images/image2.png" @some-event="hide(1)" v-show="showing1"></TeamComponent>
  <TeamComponent name="유승희" food="아이스크림" teamNum="1" srcUrl="../../public/images/image4.png" @some-event="hide(2)" v-show="showing2"></TeamComponent>
  <TeamComponent name="이성수" food="순대국밥" teamNum="1" srcUrl="../../public/images/image3.png" @some-event="hide(3)" v-show="showing3"></TeamComponent>
  <TeamComponent name="전승현" food="햄버거" teamNum="1" srcUrl="../../public/images/image1.png" @some-event="hide(4)" v-show="showing4"></TeamComponent>
</template>

<script setup>
// @ is an alias to /src
import TeamComponent from '@/components/TeamCard.vue'
import { ref } from 'vue'; 
const showing1 = ref(true);
const showing2 = ref(true);
const showing3 = ref(true);
const showing4 = ref(true);

const hide =(num) =>{
  if(num==1){
    showing1.value=false;
  }
  else if(num==2){
    showing2.value=false;
  }
  else if(num==3){
    showing3.value=false;
  }
  else if(num==4){
    showing4.value=false;
  }
  
}
</script>

