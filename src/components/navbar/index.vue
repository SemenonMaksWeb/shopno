<template>
  <div class="header__navbar">
    <div key=1 class="navbar" v-show="checkNavBar">
      <a :href="data.href" class="navbar__link" v-for="data in link" :key="data.id">{{ data.name }}</a>
    </div>
    <svg viewBox="0 0 100 100" width="80" :class="[ checkNavBar ? 'active' : '', 'ham ham6']"  v-on:click="clickNavbar">
      <path
        class="line top"
        d="m 30,33 h 40 c 13.100415,0 14.380204,31.80258 6.899646,33.421777 -24.612039,5.327373 9.016154,-52.337577 -12.75751,-30.563913 l -28.284272,28.284272" />
      <path
        class="line middle"
        d="m 70,50 c 0,0 -32.213436,0 -40,0 -7.786564,0 -6.428571,-4.640244 -6.428571,-8.571429 0,-5.895471 6.073743,-11.783399 12.286435,-5.570707 6.212692,6.212692 28.284272,28.284272 28.284272,28.284272" />
      <path
        class="line bottom"
        d="m 69.575405,67.073826 h -40 c -13.100415,0 -14.380204,-31.80258 -6.899646,-33.421777 24.612039,-5.327373 -9.016154,52.337577 12.75751,30.563913 l 28.284272,-28.284272" />
    </svg>
  </div>
</template>

<script>
    export default {
        data(){
            return{
                checkNavBar: false,
                link:[
                    {name:"About us", href: ""},
                    {name:"Featured works", href: ""},
                    {name:"Our services", href: ""},
                    {name:"Small team", href: ""},
                    {name:"What they says", href: ""},
                ]
            }
        },
      methods:{
          clickNavbar: function(){
              console.log(this.checkNavBar);
              this.checkNavBar = !this.checkNavBar;
          }

      }
    }
</script>

<style lang="sass">
  @import "style"
</style>
