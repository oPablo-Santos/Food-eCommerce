<template>
  <div>
    <v-app-bar
      color="surface"
      height="80"
      class="el"
      app
      :style="{ padding: $vuetify.breakpoint.mdAndUp ? '0px 100px' : '' }"
      ><v-toolbar-title
        @click="$router.push('/')"
        class="red--text text-md-h5 font-weight-bold pointer"
      >
        FoodNetwork
      </v-toolbar-title>
      <v-spacer />
      <v-btn nuxt to="/products" icon>
        <v-icon size="20"> mdi-store-outline</v-icon>
      </v-btn>
      <v-badge
        overlap
        :content="$store.state.cart.cart.length"
        v-if="$store.state.cart.cart.length > 0"
      >
        <v-btn nuxt to="/cart" icon>
          <v-icon size="20"> mdi-cart-outline</v-icon>
        </v-btn></v-badge
      >
      <v-btn v-else nuxt to="/cart" icon>
        <v-icon size="20"> mdi-cart-outline</v-icon>
      </v-btn>
      <v-divider vertical class="mx-md-5" />
      <v-btn @click="toggleTheme" icon>
        <v-icon size="20"> mdi-cached </v-icon>
      </v-btn>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  methods:{
    toggleTheme(){
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark
    }
  }
};
</script>

<style></style>
