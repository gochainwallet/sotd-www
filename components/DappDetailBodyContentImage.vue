<template>
  <div class="component-DappDetailBodyContentImage">
    <div class="wrapper">
      <img class="image" :src="productImage">
    </div>
  </div>
</template>

<script>
export default {
  props: {
    productImage: {
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/css/settings';

.image {
  width: 100%;
  max-width: 100%;
  display: block;
  @include tweakpoint('min-width', 1000px) {
    border-radius: 4px;
  } 
}

.wrapper {
  padding-bottom: 20px;
  @include tweakpoint('min-width', 1000px) {
    margin: 0 10px;
    padding: 0 0 25px 0;
  } 
}
</style>
