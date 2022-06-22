<template>
  <img v-bind:src="picture" alt="" />
  <h1>ຍິນດີຕ້ອນຮັບສູ່ການຂຽນເວັບ Vue JS</h1>
  <section>
    <h3>ຊື່ ແລະ ນາມສະກຸນ : {{ firtname }} {{ lastname }}</h3>
    <h3>ອາຍຸ : {{ age }} ປີ</h3>
    <h3>ຊື່ ແລະ ນາມສະກຸນ : {{ getFullname() }}</h3>
    <h3>ທີ່ຢູ່ : <span v-html="address"></span></h3>
  </section>
</template>

<script>
import image from "./assets/logo.png";
export default {
  name: "App",
  data() {
    return {
      firtname: "ແກ່ນຈັນ",
      lastname: "ຫລໍ່ບຸນທຳ",
      age: 20,
      address: "<strong>ແຂວງອຸດົມໄຊ</strong>",
      picture: image,
    };
  },
  methods: {
    getFullname() {
      return (
        this.firtname + " " + this.lastname + " ອາຍຸ : " + this.age + " ປີ"
      );
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, NotoSansLao, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
