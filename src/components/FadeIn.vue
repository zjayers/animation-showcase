<template>
  <div>
    <button class="btn btn-primary" @click="show = !show">Fade {{ show ? 'Out' : 'In' }}</button>
    <br><br>
    <transition name="fade" type="transition">
      <div v-show="show" class="alert alert-info">This is some information</div>
    </transition>
  </div>
</template>

<script>
import showMixIn from '@/mixins/showMixIn';

export default {
  name: 'FadeIn',
  mixins: [showMixIn],
};
</script>

<style>
.fade-enter {
  opacity: 0;
}

.fade-enter-active {
  transition: opacity 1s;
}

.fade-leave {
  opacity: 1;

}

.fade-leave-active {
  transition: opacity 1s;
  opacity: 0;
}
</style>
