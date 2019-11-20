<template>
  <v-flex xs12 sm6> 
    <v-card
      v-for="(result, index) in results"
      :key="index"
      class="search-result ma-3"
    > 
      <!-- EXERCISE - Format search results -->
      <v-list three-line> 
        <v-list-tile >  
        <v-list-tile-content> 
        <v-list-tile-title v-if="result.name!=''"> Name: {{result.name}} </v-list-tile-title>
        <v-list-tile-sub-title v-if="result.aliases!=''"> Alias: {{result.aliases}} </v-list-tile-sub-title>
        <v-list-tile-sub-title v-if="result.gender!=''"> Gender: {{result.gender}} </v-list-tile-sub-title>
        <v-list-tile-sub-title v-if="result.culture!=''"> Culture: {{result.culture}} </v-list-tile-sub-title>
        <v-list-tile-sub-title v-if="result.born!=''"> Date of Birth: {{result.born}} </v-list-tile-sub-title>
        <v-list-tile-sub-title v-if="result.died!=''"> Date of death: {{result.died}} </v-list-tile-sub-title>
        <v-list-tile-sub-title v-if="result.died!=''"> Allegiances: {{result.allegiances}} </v-list-tile-sub-title>
        </v-list-tile-content>
        </v-list-tile>
      </v-list>
    
    </v-card>
  </v-flex>
</template>

<script>
export default {
  name: "Results",
  props: {
    results: {
      type: Array,
      required: true
    }
  }
};
</script>

<style scoped>
  .search-result {
    min-height: 100px;
    backgorund-color: green;
    
  }
  
</style>
