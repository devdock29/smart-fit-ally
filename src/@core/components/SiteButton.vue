<script setup>
defineProps({
  outlined: {
    type: Boolean,
    default: false
  }
})
</script>

<template>
  <button
      :class="[outlined ? 'bg-transparent outline outline-2 outline-primary hover:outline-white' : 'bg-primary']"
      class="text-white rounded-4xl text-sm sm:text-base lg:text-lg 2xl:text-xl 3xl:text-2xl font-bold px-3 sm:px-5 py-2 lg:px-6 3xl:px-9.5 3xl:py-5"
  >
    <slot />
  </button>
</template>

<style scoped>
button{
  transition: all .3s ease-in;
}
button.bg-primary:hover{
  box-shadow: 0 3px 9px 1px theme('colors.primary');
  transform: translateY(-3px);
}
</style>