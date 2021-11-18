<template>
  <div class="wrapper" id="index">
    <h1 class="f_grey">貓毛輪值線上表單</h1>
    <a class="btn" href="regular.html">飲食及便便紀錄</a>
    <a class="btn" href="medicine.html">餵藥及特殊飲食紀錄</a>
  </div>
</template>

<script>
export default {
  layout: "default",
  // page component definitions
};
</script>

<style lang="scss" scoped>
#index {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  a {
    display: block;
  }
}
</style>
