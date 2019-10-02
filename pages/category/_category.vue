<template>
  <div>dc</div>
</template>

<script>
export default {
  layout: 'panel',
  created() {
    // console.log(this.$route.params.category)
    this.getNewsletter()
  },
  methods: {
    getNewsletter() {
      const newsletter = [
        { name: 'Tecnologia', suscribed: 10, target: 100 },
        { name: 'Cocina', suscribed: 10, target: 1 },
        { name: 'Negocios', suscribed: 10, target: 1 }
      ]
      this.filter(newsletter)
      // axios.get(url)
      // .then(response => {
      // this.filter(response.data)
      // })
    },
    filter(newsLetters) {
      const approved = newsLetters.filter(function(newsLetter) {
        return newsLetter.suscribed >= newsLetter.target
      })
      console.log(approved)
    }
  }
}
</script>
