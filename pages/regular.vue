<template>
  <div class="wrapper" id="regular">
    <h1>飲食及如廁紀錄表</h1>
    <el-button type="danger">danger</el-button>
    <form v-on:submit.prevent="sendMessage">
      <div class="d_flex">
        <div class="W50">
          <input type="text" id="datepicker" placeholder="請選擇日期" />
        </div>
        <div class="W50 arrow">
          <select name="time" id="">
            <option value="0" disabled selected>選擇班次</option>
            <option value="day">早班</option>
            <option value="night">晚班</option>
          </select>
        </div>
      </div>
      <div class="W100">
        <div class="d_flex record_item">
          <div class="name">大哥</div>
          <div class="detail">
            <div class="fodder d_flex">
              <p class="f_blue">乾乾</p>
              <div>
                <input type="text" class="slider" id="slider2" />
              </div>
            </div>
            <div class="can d_flex">
              <p class="f_blue">罐頭</p>
              <div>
                <input type="text" class="slider" />
              </div>
            </div>
            <div class="excretion d_flex">
              <div class="W50 d_flex">
                <p class="f_blue">尿</p>
                <div><input type="checkbox" name="pee" id="" /></div>
              </div>
              <div class="W50 d_flex">
                <p class="f_blue">屎</p>
                <input type="checkbox" name="poop" id="" />
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="W100">
        <button type="submit" class="btn">
          {{ loading ? "loading" : "送出" }}
        </button>
        <NuxtLink
          class="f_red"
          :to="{ name: 'regular', query: { date: todate } }"
          >看前班紀錄</NuxtLink
        >
        <NuxtLink class="f_red" to="/medicine">前往餵藥及特殊飲食須知</NuxtLink>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  layout: "default",
  data() {
    return {
      loading: false,
      date: "",
      time: "",
      todate: "20211118",
    };
  },
  beforeMount() {
    console.log(this.$route.query);
  },
  methods: {
    sendMessage() {
      this.loading = true;
      this.$axios
        .post("/messages", {
          name: this.name,
          email: this.email,
          phone: this.phone,
          message: this.message,
        })
        .then((response) => {
          this.success = true;
          this.errored = false;
        })
        .catch((error) => {
          this.errored = true;
        })
        .finally(() => {
          this.loading = false;
        });
    },
  },
};
</script>

<style lang="scss" scoped>
#regular {
  a {
    display: block;
  }
}
</style>
