<template>
  <div>
   <h1>Welcome to ReddIt</h1>
   <h2>{{title}}</h2>
   <input type="text" v-model="title">
   <ul>
     <li v-for="(user, index) in users" :key="index">{{user.name}}</li>
   </ul>
  </div>
</template>

<script>
import sourceData from "../../src/data.json";
console.log(sourceData.threads);
const { threads, categories, moderators, posts, stats, users } = sourceData;

export default {
  name: "HelloWorld",
  data() {
    return {
      title: "VUE APP",
      threads,
      posts,
      users
    };
  }
};
</script>
