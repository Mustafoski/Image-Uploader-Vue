<template>
  <div>
    <img :src="image.link" v-for="image in allImages" :key="image" />
  </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex';
export default {
  name: 'ImageList',
  created() {
    this.fetchImages();
  },
  methods: {
    ...mapActions(['fetchImages']),
    ...mapGetters(['allImages']),
  },
};
</script>

<style scoped></style>
