<template>
  <div class="centered">
    <form>
      <h4>Создание поста</h4>
      <input type="text" placeholder="Title" />
      <input type="text" placeholder="Description" />
      <button>Add</button>
    </form>
    <div class="posts">
      <div class="post" v-for="(post, i) of posts" :key="i">
        <div><strong>Название:</strong> {{ post.title }}</div>
        <div><strong>Описание:</strong> {{ post.description }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {
          id: 1,
          title: 'Title 1',
          description: 'Description 1'
        },
        {
          id: 2,
          title: 'Title 2',
          description: 'Description 2'
        },
        {
          id: 3,
          title: 'Title 3',
          description: 'Description 3'
        }
      ]
    }
  },
  methods: {
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
  }
  body {
    margin: 0;
  }
  .centered {
    width: 900px;
    margin-left: auto;
    margin-right: auto;
    padding: 10px;
  }
  form {
    margin-bottom: 20px;
  }
  h4 {
    margin-bottom: 10px;
  }
  .post {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 10px;
    margin-bottom: 10px;
    
  }
</style>