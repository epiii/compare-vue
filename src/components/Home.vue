<template>
  <div class="home">
    Home
    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            {{heading}}
          </h1>
          <div class="is-two-thirds column is-paddingless">
            <h2 class="subtitle is-4">
              {{subheading}}
            </h2>
          </div>
          <a class="button is-large is-primary">Learn more</a>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'home',
  data
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
    @import '../mq'
</style>
