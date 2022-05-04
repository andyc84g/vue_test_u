<template>
  <div>
    <ul>
      <li v-for="user in userList" :key="user.id"> <a  @click.prevent="onClick(user)">{{ user.name }} </a></li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userList: [
        { name: 'andy', id: 1 },
        { name: 'andy2', id: 2 },
        { name: 'andy3', id: 3 },
      ],
    };
  },
  methods:{
      onClick(user){
        //   console.log(this)
          this.$router.push(`/users/${user.name}`)
      }
  }
};
</script>

<style lang="less" scoped>
a{
    cursor: pointer;
}
</style>
