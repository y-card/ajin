<script setup lang="ts">
import Divider from "./atom/Divder.vue";

const props = defineProps({
  type: String,
});

let title = "";
let description =
  "처음으로 경험해보는 부모라는 역할은<br/>서툴기도, 때론 버겁기도 했지만<br/><br/>존재만으로도 행복을 주는 아진이가 있어<br/>일년동안 더없이 기쁜 날들이었습니다.<br/><br/>하나님이 주신 가장 큰 선물 아진이가<br/>저희 품에 온지 어느덧 일년이 되어<br/><br/>그동안 보내주신 관심과 사랑에<br/>감사하는 마음으로 작은 잔치를 마련했습니다.<br/><br/>바쁘시더라도 소중한 시간 내주셔서<br/>밝고 건강한 아이로 자랄 수 있도록<br/>축복해주시면 감사하겠습니다.<br/><br/><em class='parents-name'>아빠 조재국, 엄마 반가운 올림</em>";
</script>

<template>
  <div :class="['main_comment', type]">    
    <Divider />
  </div>
  <div :class="['invitation', type]">
      <div class="fade-in">
        <div class="date">
          <p class="date_comment" v-html="title"></p>
          <p>2025년 3월 8일 오전 11시 30분</p>
          <p>플로렌스 위례점</p>
        </div>
      <p class="comment" v-html="description"></p>
    </div>
  
  </div>
</template>

<style scoped>
.main_comment,
.invitation {
  position: relative;
  font-family: "Nanum Myeongjo", serif;
  font-weight: bolder;
  text-align: center;
  line-height: 2rem;
  color: var(--vt-c-black-soft);
  font-weight: 400;
  text-align: center;
  letter-spacing: -0.5px;
  font-size: 18px;
}

.invitation .date {
  color: var(--vt-c-beige-dark);
}

.invitation .date_comment {
  /* font-size: 18px; */
}

.invitation .comment {
  margin: 2rem 0 3rem;
}

.names p {
  font-family: "Nanum Myeongjo", serif;
  color: var(--vt-c-beige-dark);
  font-weight: 500;
  line-height: 25px;
}

.names em {
  font-style: normal;
  font-size: 15px;
  color: var(--vt-c-black-mute);
}

.comment:deep .parents-name{
  font-style: normal;
  font-weight: 700;
}
</style>
