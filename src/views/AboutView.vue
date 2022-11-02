<script>
export default {
  data() {
    return {
      gotCharacters: [],
      zaehler: 0,
      kunden: [{
          id: "35",
          firstName: "Peter",
          lastName: "Müller",
          isPremium: true,
          hasCredits: null,
          age: 54,
        },
        {
          id: "36",
          firstName: "Maxima",
          lastName: "Powers",
          isPremium: false,
          hasCredits: null,
          age: 24,
        },
      ]
    }
  },
  methods: {
    holeDaten() {
      this.zaehler++;
      this.kunden[1].firstName = "Andre"
      //axios.get('https://thronesapi.com/api/v2/Characters')...
      this.gotCharacters = response.data;
    }
  }
}
</script>
<template>
  <div class="about">
    <h1>Ich zähle: {{ zaehler }} </h1>
    <button @click="holeDaten">Test</button>




    <li v-bind:key="kunde.id" v-for="kunde in kunden">
      <ProfilePictureComponent customer="kunde" />
    </li>





  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
