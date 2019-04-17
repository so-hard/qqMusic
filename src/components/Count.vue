<template>
  <div class="add">
    <button type="button" v-on:click="add">+1</button>
    <button type="button" @click="cut">-1</button>
    <!-- <p>{{modelCount}}</p> -->
  </div>
</template>

<script>
export default {
  name: 'Count',
  data(){
    return {
      // data: 0,
      // datap: msg
      // aP: this.props.msg
    }
  },

  // props: ['modelCount'],

  methods:{
    add(){
      this.$store.state.homeModelCount += 1;
    },

    cut(){
      this.$store.state.homeModelCount-=1;
    }
  },

  computed: {
  //   modelCount(){
  //   return 
  // }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
h3
  margin 40px 0 0

ul
  list-style-type none
  padding 0

li
  display inline-block
  margin 0 10px

a
  color #42b983
</style>
