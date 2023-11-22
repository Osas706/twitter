<template>
  <div class="home">
    <Tweet v-for="tweet in tweets" :key="tweet._id" :tweet="tweet"/>
  </div>
</template>
 
<script>
import { ref } from 'vue'
import vweets from '../vweets'
import Tweet from '@/components/Tweet.vue';

export default {

  setup() {
    const tweets = ref(vweets);

    return{
      tweets ,
      Tweet
    }
  },
  components: {
    Tweet
  }
}
</script>
