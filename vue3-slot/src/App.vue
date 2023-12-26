<template>
  <alt-bilesen>
    <template v-slot:form-header>
      <h2>Giriş Formu</h2>
    </template>

    <template v-slot:form-elements>
      <label for="email">E-Posta</label>
      <input type="email" v-model="email" placeholder="E-posta adresinizi giriniz">

      <label for="password">Şifre</label>
      <input type="password" v-model="password" placeholder="Şifrenizi giriniz">
      <h2>E-postanız : {{ email }}</h2>
      <h2>Şifreniz : {{ password }}</h2>
    </template>

    <template v-slot:form-control>
      <button>Giriş Yap</button>
    </template>
  </alt-bilesen>
</template>

<script>
import altBilesen from './components/alt-bilesen.vue';

export default {
  components: {
    "alt-bilesen": altBilesen
  },
  data() {
    return {
      email: "",
      password: ""
    }
  }
}
</script>
