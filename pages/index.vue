<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card class="logo py-4 d-flex justify-center">
        <NuxtLogo />
        <VuetifyLogo />
      </v-card>
      <v-card>
        <v-card-title class="headline">
          Welcome to the Vuetify + Nuxt.js template
        </v-card-title>
        <v-card-text>
          <p>Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
          <p>
            For more information on Vuetify, check out the <a
              href="https://vuetifyjs.com"
              target="_blank"
              rel="noopener noreferrer"
            >
              documentation
            </a>.
          </p>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            Continue
          </v-btn>
        </v-card-actions>
        <v-divider></v-divider>
        <v-card-text>
          <h3>...</h3>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>


<script>
export default{
  name: 'IndexPage',
  title: 'Home',
  data () {
    return {
      var:null,
    }
  },
  methods: {
    test(){
      // method test
    }
  },
  async created(){
    // 1. Load the service
    await this.$fire.authReady()
    // 2. Use the service
    await this.$fire.auth.createUserWithEmailAndPassword('foo@foo.foo','test')
  }
}
</script>
