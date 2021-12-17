<template>
  <h1>ຍິນດີຕ້ອນຮັບສູ່ການຂຽນເວັບ Vue JS</h1>
  <section>
    <h3>ຊື່ ແລະ ນາມສະກຸນ : {{ firtname }} {{ lastname }}</h3>
    <h3>ຊື່ ແລະ ນາມສະກຸນ : {{ getFullname() }}</h3>
    <h3>ອາຍຸ : {{ age }} ປີ</h3>
    <span v-html="address"></span>
  </section>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firtname: "ແກ່ນຈັນ",
      lastname: "ຫລໍ່ບຸນທຳ",
      age: 20,
      address: "<address>ທີ່ຢູ່ : ແຂວງອຸດົມໄຊ</address>",
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
  font-family: Avenir, noto sans lao, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
