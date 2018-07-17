<template>
  <div>
   <h1>Welcome to ReddIt</h1>
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
      threads,
      posts,
      users
    };
  }
};
</script>
