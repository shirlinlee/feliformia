<template>
  <div>
    <nuxt />
    <NuxtLogo />
  </div>
</template>

<style lang="scss">
$red: #b33a39;
$grey: #657181;
$blue: #6da2c2;
$light_grey: #f5f7f8;
$brown: #8e8783;

body,
html {
  height: initial !important;
  width: 100%;
  overflow-x: hidden;
  font-family: "Noto Sans TC", "Helvetica Neue", Helvetica, sans-serif;
  text-align: center;
  font-size: 15px;
  min-height: 100vh;
  position: relative;
}

* {
  box-sizing: border-box;
}

.wrapper {
  width: 100%;
  max-width: 450px;
  margin: 0 auto;
  padding: 30px 20px;
}

.W20 {
  width: 20%;
}

.W25 {
  width: 25%;
}

.W33 {
  width: 33%;
}

.W50 {
  width: 50%;
}

.W67 {
  width: 67%;
}

.W75 {
  width: 75%;
}

.f12 {
  font-size: 12px;
}

.f15 {
  font-size: 15px;
  line-height: 1.5;
}

.f19 {
  font-size: 19px;
  line-height: 1.3;
}

.bg_cover {
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}

.f_white {
  color: #fff;
}

.f_grey {
  color: $grey;
}

.f_red {
  color: $red;
}

.f_blue {
  color: $blue;
}

.bg_red {
  background-color: $red;
}

.bg_blue {
  background-color: $blue;
}

.f_b {
  font-weight: bold;
}

.t_center {
  text-align: center;
}

.t_left {
  text-align: left;
}

.d_flex {
  display: flex !important;
  flex-wrap: wrap;
}

.d_none {
  display: none;
}

.mb {
  display: none;
}

.pc {
  display: inline-block;
}

.ham {
  display: none;
}

button,
input,
select {
  -webkit-appearance: none;
  background-color: transparent;
  border: none;
  border: 1px solid $brown;
  height: 50px;
  line-height: 50px;
  padding: 0 10px;
  width: 100%;
  color: #444;
  font-size: 15px;
}

input[type="checkbox"] {
  height: 40px;
  width: 40px;
  &:checked {
    background-image: url(/images/v.svg);
    background-size: 80%;
    background-position: center;
    background-repeat: no-repeat;
  }
}

.arrow {
  position: relative;
  &:after {
    content: "";
    border-top: 12px solid $grey;
    border-left: 10px solid transparent;
    border-right: 10px solid transparent;
    position: absolute;
    right: 15px;
    top: 50%;
    transform: translate(0, -50%);
    display: block;
  }
}

h1 {
  font-size: 23px;
  font-weight: 500;
  margin-bottom: 30px;
}

a {
  text-decoration: underline;
  margin-bottom: 15px;
}

.btn {
  background-color: $red;
  color: #fff;
  font-size: 17px;
  font-weight: 500;
  padding: 20px;
  text-decoration: none;
  margin-bottom: 20px;
  border-radius: 30px;
}

.d_flex {
  justify-content: space-between;
  .W50 {
    width: calc(50% - 10px) !important;
    margin-bottom: 20px;
  }
}

.ui-state-default {
  border: none !important;
  padding: 5px 0.2em !important;
  margin: 2px 0;
  text-align: center !important;
  &.ui-state-highlight {
    border: none;
    background-color: $blue;
    color: #fff;
  }
  &.ui-state-active {
    background-color: $red;
  }
}

.rs-container {
  .rs-selected {
    background-color: $blue;
  }
}

.record_item {
  align-items: center;
  .name {
    width: 80px;
  }
  .detail {
    width: calc(100% - 80px);
    > div {
      margin-bottom: 10px;
    }
    .W50 {
      > * {
        display: inline-block;
        vertical-align: middle;
      }
      p {
        // margin-right: 20px;
      }
    }
    .d_flex {
      p {
        width: 50px;
      }
      > div {
        width: calc(100% - 80px);
      }
    }
  }
  .excretion {
    .d_flex {
    }
  }
}

.rs-container {
  * {
    text-align: left;
  }
}

@media screen and (max-width: 600px) {
  .mb {
    display: inline-block;
  }

  .pc {
    display: none;
  }
}
</style>
