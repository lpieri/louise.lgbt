<template>
  <div>

    <h2 class="title is-2">Contact :</h2>

    <div class="columns is-centered">
      <div class="contact-div column is-one-fifth" v-for="contact in contactData">
        <figure class="contact-logo image is-64x64 is-rounded">
          <a :href="contact.link">
            <img :src="require(`../assets/${contact.logo}`)">
          </a>
        </figure>
      </div>
    </div>

    <div class="field is-grouped is-grouped-centered">
      <div class="control">
        <button class="button is-rounded" @click="this.$parent.closeModal">Cancel</button>
      </div>
    </div>

  </div>
</template>

<script>
  export default {
    name: 'ContacInfo',
    data () {
      return {
        contactData: {
          "github": {
            logo: "github.png",
            link: "https://github.com/lpieri"
          },
          "linkedin": {
            logo: "linkedin.png",
            link: "https://www.linkedin.com/in/lpieri/"
          },
          "malt": {
            logo: "malt.png",
            link: "https://www.malt.fr/profile/delay"
          },
          "twitter": {
            logo: "twitter.png",
            link: "https://twitter.com/louise_tech_"
          },
          "mail": {
            logo: "gmail.png",
            link: "mailto:contact@louise.tech"
          }
        }
      }
    },
    methods: {
    }
  }
</script>


<style>
  .contact-logo {
    display: flex!important;
    align-items: center;
  }

  .contact-div {
    display: flex!important;
    justify-content: center;
  }
</style>
