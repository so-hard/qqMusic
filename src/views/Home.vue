<template>
  <div class="home">
    <Count  v-bind:modelCount="modelCount"/>
    <Model v-for="n in modelCount"
           v-bind:key="n.id"
     />
     {{modelCount}}
  </div>
</template>

<script>
// @ is an alias to /src
import Count from '../components/Count.vue'
import Model from '../components/Model.vue'

export default {
  name: 'home',
  components: {
    Count,
    Model
  },

  data(){
    return{
      datas: [1,2,3],
    }
  },

  methods:{
  },

  computed:{
    modelCount() {
      return this.$store.state.homeModelCount
    }
  }
}
</script>
