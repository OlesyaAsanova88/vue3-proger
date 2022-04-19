<template>
  <div>
    <form @submit.prevent>
      <h4>Создание поста</h4>

      <my-input v-model="post.title" type="text" placeholder="название" />

      <my-input v-model="post.body" type="text" placeholder="описание" />

      <my-button class="btn" style="margin-top: 15px" @click="createPost"
        >Создать</my-button
      >
    </form>
  </div>
</template>


<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: "",
        body: "",
      };
    },
  },
};
</script>



   <style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}
form {
  display: flex;
  flex-direction: column;
}
.post {
  margin-top: 15px;
  padding: 15px;
  border: 2px solid teal;
}
</style>
