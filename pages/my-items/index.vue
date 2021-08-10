<template>
  <div>
    <MyItem 
        v-for="item in myRentals"
        :key="item.id"
        :item="item"
    />
  </div>
</template>

<script>
import { mapState } from 'vuex';
  export default {
    layout: "no-nav",
    computed: {
      ...mapState(['myRentals'])
    }
  }
</script>

<style scoped>
 .item-container {
    display: flex;
    margin: 3rem 0
}
.text-container {
    padding: 0 1rem
}
img {
    width: 17.5rem;
    border-radius: 0.5rem;
    height: 11rem
}
p {
    font-size: 0.8rem;
    color: grey
}
</style>