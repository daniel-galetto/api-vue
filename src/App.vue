<template>
  <div class="container"> 
    <h1>Api Rick and Morty</h1>
    <FilterByStatus />
    <FilterByName />
    <ListCharacters />
  </div>
</template>

<script>
import FilterByName from '@/components/FilterByName'
import ListCharacters from '@/components/ListCharacters'
import FilterByStatus from '@/components/FilterByStatus'
export default {
  name: 'App',
  components: {
    ListCharacters,
    FilterByStatus,
    FilterByName,
   
  }
}
</script>

<style lang="scss">
 
* {
   box-sizing: border-box;
   margin: 0;
   padding: 0;
}

body { 
  background-color: rgb(26, 29, 46);
  color: white;
  font-family: "Helvetica Neue",
}

h1 {
  margin-bottom: 3rem;
  text-align: center;
}

.container {
  width: 980px;
  max-width: 90%;
  margin: 5rem auto;
}

img {
  width: 100%;
}

</style>
