<template>
  <div>
    <div class="user-header">
      <h4 class="title">User details for:{{ user.title }}</h4>
    </div>

    <h5>User details:</h5>
    <h6>User ID: {{ user.id }}</h6>
    <h6>User name: {{ user.user.name }}</h6>
    <img :src="user.picture" />
    <div>
      <BaseIcon name="map"> <h4>Location</h4> </BaseIcon><br />
      <address>{{ user.location }}</address>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    user: {
      type: Object,
      required: true,
    },
  },
}
</script>
<style scoped>
.location {
  margin-bottom: 0;
}
.location > .icon {
  margin-left: 10px;
}
.user-header > .title {
  margin: 0;
}
.list-group {
  margin: 0;
  padding: 0;
  list-style: none;
}
.list-group > .list-item {
  padding: 1em 0;
  border-bottom: solid 1px #e5e5e5;
}

img {
  width: 100%;
  max-width: 100px;
}
</style>
