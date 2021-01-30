<template>
  <div id="app">
    <div class="container-app">
      <div class="container-quiz">
    <Search />
    <User />
    </div>
    </div>
  </div>
</template>

<script>
import Search from './components/Search';
import User from './components/User';

export default {
  name: 'app',
  components: {
    User,
    Search
  }
};
</script>

<style lang="stylus">
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  font-smoothing antialiased
  margin 10px
</style>
