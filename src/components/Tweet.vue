<template>
  <div className="tweet">
    <profile-image :image="tweet.user.image" />

    <div className="body">
      <div className="top">
        <user :user="tweet.user" />
        <timestamp :timestamp="tweet.timestamp" />
      </div>
      <message :message="tweet.message" />
      <actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";

export default {
  props: ["tweet"],
  components: { ProfileImage, User, Timestamp, Message, Actions },
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
