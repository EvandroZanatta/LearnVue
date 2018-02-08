<template>
  <div class="navbar-header ">
        <router-link to="/" class="navbar-brand">SocialC</router-link>
        <a href="/" class="navbar-brand">SocialC</a>
        <button class="navbar-toggle" type="button" data-toggle="collapse" data-target="#navbar-main" @click.prevent="toggleNavBarCollapse">
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
        </button>
  </div>
</template>

<script>
    export default {
        name: "header-nav-brand",
        data (){
            return {}
        },
        methods: {
            toggleNavBarCollapse (){
                this.$emit('NavBarCollapseAction')
            }
        }
    }
</script>