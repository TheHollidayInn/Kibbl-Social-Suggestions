<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class='tweet' v-for='tweet in tweets'>
      <p><strong>{{tweet.account}}</strong></p>
      <p><span>{{tweet.text}}</span></p>
      <p><a :href='tweet.url' target='_blank'>{{tweet.url}}</a></span></p>
      <p><span><img :src='tweet.img' /></span></p>
    </div>
  </div>
</template>

<script>
import tweets from '../data/tweets.json'

export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Social Suggestions',
      tweets,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }

  .tweet {
    max-width: 600px;
    margin: 0 auto;
    background: #fff;
    padding: 1em;
    margin-bottom: 1em;
  }

  .tweet img {
    max-width: 100%;
  }
</style>
