<template>
    <div class="posts">
        <h1>{{ post.title }}</h1>
        <h2>{{ post.description }}</h2>
    </div>
</template>

<script>
import PostsService from '@/services/WebSocket'
export default {
  name: 'post',
  data () {
    return {
      post: []
    }
  },
  mounted () {
    this.getPosts()
  }
}
</script>
<style type="text/css">
.table-wrap {
  width: 60%;
  margin: 0 auto;
  text-align: center;
}
table th, table tr {
  text-align: left;
}
table thead {
  background: #f2f2f2;
}
table tr td {
  padding: 10px;
}
table tr:nth-child(odd) {
  background: #f2f2f2;
}
table tr:nth-child(1) {
  background: #4d7ef7;
  color: #fff;
}
a {
  color: #4d7ef7;
  text-decoration: none;
}
a.add_post_link {
  background: #4d7ef7;
  color: #fff;
  padding: 10px 80px;
  text-transform: uppercase;
  font-size: 12px;
  font-weight: bold;
}
</style>
