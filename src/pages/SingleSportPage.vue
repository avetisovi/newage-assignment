<template>
  <section class="singleSport">
    <h1 class="singleSport__title">{{ singleSport.n }}</h1>
  </section>
</template>

<script>
import { mapGetters, mapMutations } from 'vuex';
export default {
  computed: {
    ...mapGetters({
      singleSport: 'sports/singleSport'
    })
  },
  methods: {
    ...mapMutations({
      setSlug: 'sports/setSlug'
    })
  },
  mounted() {
    this.setSlug(this.$route.params.slug);
  }
};
</script>

<style lang="scss">
.singleSport {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}
</style>
