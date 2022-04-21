<template>
  <div class="navbar">
    <div @click="$router.push('/')" style="color: teal">ГУАП на Vue3</div>
    <div class="navbar__btns">
      <my-button @click="$router.push('/posts')" style="margin-left: 10px">
        Posts
      </my-button>
      <my-button @click="$router.push('/about')" style="margin-left: 10px">
        About us
      </my-button>
    </div>
  </div>
</template>


<script>
export default {};
</script>

<style scoped>
.navbar {
  height: 50px;
  background-color: rgba(250, 247, 74, 0.171);
  box-shadow: 0 0 15px teal;

  display: flex;
  align-items: center;
  padding: 0 15px;
  justify-content: space-between;
}
.navbar__btns {
}
</style>