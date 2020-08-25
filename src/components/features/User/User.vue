<template>
  <div>
    <div class="d-flex flex-row">
      <transition appear name="left">
        <shop class="w-75"></shop>
      </transition>
      <transition appear name="right">
        <cart class="w-25"></cart>
      </transition>
    </div>
  </div>
</template>

<script>
import Shop from './Shop/Shop';
import Cart from './Cart/Cart';

export default {
  components: {
    Shop,
    Cart
  }
}
</script>

<style scoped>
  @keyframes fromleft {
    from {
      opacity: .3;
      transform: translateX(-20px);
    }
    to {}
  }

  @keyframes fromright {
    from {
      opacity: .3;
      transform: translateX(20px);
    }
    to {}
  }

  .left-enter-active {
    animation: fromleft 1s;
  }

  .right-enter-active {
    animation: fromright 1s;
  }
</style>