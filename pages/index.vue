<template>
  <v-container>
    <v-layout row wrap>
      <v-flex xs12 md6 offset-md3>
        <h1>Search iTunes</h1>
        <br />
        <v-form @submit.prevent="submit">
          <v-text-field
            placeholder="Enter Artist Name"
            v-model="search"
            autofocus
          ></v-text-field>
        </v-form>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>

export default {
  data() {
    return {
      search: '',
    };
  },
  methods: {
    submit(event) {
      this.$router.push(`results/${this.search}`);
    },
  }
};
</script>
