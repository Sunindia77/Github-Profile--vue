<template>
  
    
      <div>
        <h1>GitHub User Finder</h1>
        <br/>
        <input
          v-model="query"
          @input="debouncedSearch"
          placeholder="Enter username"
        />
      </div>
  

</template>


<script>
import { mapActions, mapState } from "vuex";
import debounce from "lodash/debounce";

export default {
  name: "search",
  computed: {
    ...mapState(["searchQuery"]),
    query: {
      get() {
        return this.searchQuery;
      },
      set(val) {
        return this.setSearchQuery(val);
      },
    },
  },
  methods: {
    ...mapActions(["setSearchQuery", "search"]),
    debouncedSearch: debounce(function () {
      this.search();
    }, 500),
  },
};
</script>

<style lang="stylus" scoped>
input {
  width: 40%;
  font-size: 16px;
  text-align: center;
  margin-top:50px;
}
 h1 {
   margin-top: 20px;
  color :green;


 }
</style>
