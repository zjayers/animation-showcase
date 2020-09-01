<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <h1>Animations</h1>
        <hr>
        <fade-in></fade-in>
        <slide-in></slide-in>
      </div>
    </div>
  </div>
</template>

<script>
import SlideIn from '@/components/FadeIn.vue';
import FadeIn from '@/components/SlideIn.vue';

export default {
  components: {
    FadeIn,
    SlideIn,
  },
};
</script>

<style>

</style>
