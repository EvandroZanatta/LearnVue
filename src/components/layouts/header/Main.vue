<template>
  <nav class="navbar navbar-inverse navbar-fixed-top">
      <div class="container">
        <!-- Aqui ficará nosso componente nav-brand !-->
        <nav-brand @NavBarCollapseAction="changeNavBarCollapseIn" />
        <div class="navbar-collapse collapse" id="navbar-main" :class="{in: navBarCollapseIn}">
          <!-- Aqui ficará nav-left e nav-right !-->
          <nav-left />
          <nav-right />
        </div>
      </div>
  </nav>
</template>
<script>
    import NavBrand from './NavBrand'
    import NavLeft from './NavLeft'
    import NavRight from './NavRight'

    export default {
        name: "header-main",
        components: {
            NavBrand,
            NavLeft,
            NavRight
        },
        data() {
            return {
                navBarCollapseIn: false
            }
        },
        methods: {
            changeNavBarCollapseIn () {
                this.navBarCollapseIn = !this.navBarCollapseIn
            }
        }
    }
</script>