<template>
  <button
    class="kj-btn"
    :class="[
      model === 'success'
        ? 'kj-btn--green'
        : model === 'error'
        ? 'kj-btn--red'
        : model === 'warning'
        ? 'kj-btn--yellow'
        : null,

      outlined ? 'outlined' : null,
    ]"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    model: String,
    outlined: Boolean,
  },
};
</script>

<style lang="scss" scoped>
$colors: ('green', 'yellow', 'red', 'indigo', 'blue', 'purple', 'pink');

.kj-btn {
  @apply inline-flex place-items-center justify-center
        px-6 md:px-8 py-3 md:py-4 rounded
        transform duration-200 
        hover:-translate-y-1 focus:-translate-y-1 transition-all
        font-semibold;

  @each $color in $colors {
    &--#{$color} {
      @apply bg-#{$color}-500 text-black 
        hover:bg-#{$color}-400 focus:bg-#{$color}-400;

      &.outlined {
        @apply text-#{$color}-700 bg-transparent;
      }
    }
  }
}
</style>