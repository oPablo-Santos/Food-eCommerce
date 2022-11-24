<template>
  <v-card rounded="lg" class="pa-md-10 pa-5 text-center" color="primary" dark>
    <h2 class="text-md-h3">Mais novidades e promoções?</h2>
    <p class="text-md-h6 mt-5">Inscreva-se e fique por dentro de tudo!</p>
    <br />
    <v-sheet color="transparent" class="mx-auto" max-width="400">
      <v-text-field label="Email" type="email" outlined v-model="email"></v-text-field>
      <v-btn @click="submit" outlined min-height="50" block> Inscreva-se </v-btn>
    </v-sheet>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      email: null,
    };
  },
  methods: {
    async submit() {
      await this.$swal({
        title: "Obrigado pela inscrição",
        icon: "success",
        allowOutsideClick: false,
        allowEscapeKey: false,
        timer: 4000,
        timerProgressBar: true,
        text: "Você será notificado sobre as novidades",
      });
    },
  },
};
</script>

<style></style>
