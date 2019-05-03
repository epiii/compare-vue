<template>
  <div id="app">
    <!-- navbar  -->
    <nav class="navbar has-shadow" role="navigation" aria-label="main navigation">
      <!-- logo  -->
      <div class="navbar-brand">
        <a class="navbar-item">Elfrilancer</a>
        <a
          v-on:click="toggleNav"
          v-bind:class="{'is-active':isActive}"
          role="button"
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="navMenu"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
      <!-- end of logo  -->

      <!-- menu -->
      <div id="navMenu" v-bind:class="{'is-active':isActive}" class="navbar-menu">
        <div class="navbar-end">
          <router-link to="/" class="navbar-item r-item">Home</router-link>
          <router-link to="faq" class="navbar-item r-item">Feature</router-link>
          <router-link to="faq" class="navbar-item r-item">About</router-link>
          <router-link to="faq" class="navbar-item r-item">FAQ</router-link>

          <div class="navbar-item">
            <p class="control">
              <a class="button is-primary is-outlined">
                <span class="icon">
                  <i class="fa fa-download"></i>
                </span>
                <span>Join Now</span>
              </a>
            </p>
            <!-- </div> -->
          </div>
        </div>
      </div>
      <!-- end of menu -->
    </nav>
    <!-- end of navbar -->
    <router-view/>

    <footer class="footer has-text-centered">
      <div class="container is-primary">
        <div class="columns">
          <div class="column">
            <p>iki footer... bla bla bla bla</p>
          </div>
        </div>
      </div>
    </footer>
    
  </div>
</template>

<script>
  export default {
    // name: 'App'
    name: "app",
    data: function() {
      return {
        isActive: false
      };
    },
    methods: {
      toggleNav: function() {
        this.isActive = !this.isActive;
      }
    }
  };
</script>

<style lang="sass">
  @import '../node_modules/bulma/bulma.sass'
  @import 'mq'
  // @import 'debugger'

  .navbar 
    background-color: #383838
    color: white  
    a:hover
      color: white  
      background-color:  grey 
  
  // .nav-left a 
  .navbar-item a 
    color: #fff
    font-weight: bold

  a.r-item
    color: #C1C1C1
    padding: 0.5rem 1.75rem
    +mobile 
      color: gray
      &:hover
        background-color : #F1F1F1
  
  // .footer
  //   background-color: turquoise
    // $footer-background-color:$white-bis
  // #app
  //   font-family: 'Avenir', Helvetica, Arial, sans-serif
  //   -webkit-font-smoothing: antialiased
  //   -moz-osx-font-smoothing: grayscale
  //   text-align: center
  //   color: #2c3e50
  //   margin-top: 60px
</style>
