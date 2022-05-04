<template>
    <div>
        user {{ this.$route.params.id }}
    </div>
</template>

<script>
    export default {
      beforeRouteUpdate(to, from ,next){
          console.log('to', to, 'from', from)
          setTimeout(() => {
              next()
          }, 10000);
          
      }
    }
</script>

<style lang="less" scoped>

</style>