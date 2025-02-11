<script setup lang="ts">
import img from "../assets/image/main.png";

const props = defineProps({
  type: String,
});
</script>

<template>
  <div :class="['main_visual', props.type, 'fade-in']">
    <img :src="img" class="main" />
    <p class="main_title">1st birthday</p>
    <p class="main_name">조아진</p>
    <p class="description">첫 생일파티에 초대합니다</p>
  </div>
</template>

<style scoped>
.main_visual {
  position: relative;
  font-family: "Nanum Myeongjo", serif;
  text-align: center;
  min-height: 500px;
}

.main_visual .main {
  width: auto;
  min-height: 500px;
  max-height: 813px;
  transform: translateX(-50%);
  margin-left: 50%;
}

.main_visual .main_title,
.main_visual .main_name,
.main_visual .description,
.main_visual .footer {
  position: absolute;
  left: 0;
  right: 0;
  top: 18px;
  margin: 0 auto;
  color: #fff;
  text-align: center;
  font-size: 20px;
  font-weight: bolder;
  line-height: 50px;
}
.main_visual .main_name {
  position: absolute;
  top: 75px;
  font-size: 45px;
  letter-spacing: 2px;
  color: #333;
  line-height: 60px;
}

.main_visual .description {
  top: 125px;
  font-size: 18px;
  color: #333;
}

.main_visual .footer {
  bottom: 50px;
  top: unset;
  line-height: normal;
  font-size: 13px;
  color: #333;
}

.subtitle {
  margin-bottom: 20px;
  font-size: 20px;
}

.bottom {
  position: absolute;
  bottom: 30px;
  font-size: 20px;
  width: 100%;
}

@media (min-width: var(--breakpoint)) {
}
</style>
