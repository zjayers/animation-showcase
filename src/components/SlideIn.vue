<template>
  <div>
    <button class="btn btn-primary" @click="show = !show">Slide {{ show ? 'Out' : 'In' }}</button>
    <br><br>
    <transition name="slide" type="animation">
      <div v-show="show" class="alert alert-info">This is some information</div>
    </transition>
  </div>
</template>

<script>
import showMixIn from '@/mixins/showMixIn';

export default {
  name: 'SlideIn',
  mixins: [showMixIn],
};
</script>

<style scoped>
.slide-enter {
  opacity: 0;
  transform: translateY(20px);
}

.slide-enter-active {
  transition: opacity 1s;
  animation: slide-in 1s ease-out forwards;
}

.slide-leave {
  transform: translateY(0);
}

.slide-leave-active {
  transition: opacity 1s;
  opacity: 0;
  animation: slide-out 1s ease-out forwards;
}

@keyframes slide-in {
  from {
    transform: translateY(20px);
  }
  to {
    transform: translateY(0);
  }
}

@keyframes slide-out {
  from {
    transform: translateY(0);
  }
  to {
    transform: translateY(20px);
  }
}
</style>
