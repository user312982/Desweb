<template>
  <div id="app">
    <userLogin v-if="!isLoggedIn" @loginSuccess="isLoggedIn = true" ></userLogin><!-- SOAL: tambahkan tag html sebelum directive berupa variabel yang di import di bagian script-->
    <userDashboard v-else @logout="isLoggedIn = false" ></userDashboard><!-- SOAL: tambahkan tag html sebelum directive berupa variabel yang di import di bagian script-->
  </div>
</template>

<script>
import userLogin from './components/UserLogin.vue'; //SOAL: Definisikan variabel import
import userDashboard from './components/UserDashboard.vue'; //SOAL: Definisikan variabel import

export default {
  name: 'App',
  components: {
    // SOAL: panggil components yang akan digunakan
    userLogin,userDashboard
  },
  data() {
    return {
      isLoggedIn: false
    };
  }
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
}
</style>