<script setup lang="ts">
  const posts = [
    {id: 1, title: "Пост номер 1", description: "Текст поста номера 1"},
    {id: 2, title: "Пост номер 2", description: "Текст поста номера 2"},
    {id: 3, title: "Пост номер 3", description: "Текст поста номера 3"},
  ]
</script>

<style>
* {
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
    box-sizing: border-box;
}

.post_title {
    color: black;
    font-weight: 700;
    font-size: 20px;
}

.post_description {
    color: #1c1c1c;
    font-size: 15px;
}

.post {
    border: 1px solid whitesmoke;
    border-radius: 5px;
    padding: 10px;
}

.posts {
    display: flex;
    flex-direction: column;
    gap: 10px;
}
</style>

<template>
<div id="post-site">
    <div class="posts">
        <div class="post" v-for="post in posts">
            <p class="post_title">{{ post.title }}</p>
            <p class="post_description">{{ post.description }}</p>
        </div>
    </div>
</div>
</template>