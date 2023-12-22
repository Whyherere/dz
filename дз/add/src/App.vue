<template>
  <div>
    <input v-model="firstInp" type="text">
    <input v-model="secondInp" type="text">
    <button @click="swapInp">Наоборот</button>
  </div>
  <br>
  <div>
    <input v-model="thirdInp" type="text">
    <button @click="third">Нажми</button>
    <p>{{ surname }}</p>
    <p>{{ name }}</p>
    <p>{{ patronymic }}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      firstInp: '',
      secondInp: '',
      surname: '',
      name: '',
      patronymic: '',
    };
  },
  methods: {
    swapInp() {
      const temp = this.firstInp;
      this.firstInp = this.secondInp;
      this.secondInp = temp;
    },
    third() {
      const [surname, name, patronymic] = this.thirdInp.split(' ');
      this.surname = surname;
      this.name = name;
      this.patronymic = patronymic;
    }
  },
};
</script>
<style></style>
