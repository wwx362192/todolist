<template>
    <li @click="handerDelet">{{content}}</li>
</template>

<script>
export default {
  props:['content','index'],
  methods:{
    handerDelet(){
      this.$emit('del',this.index);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
