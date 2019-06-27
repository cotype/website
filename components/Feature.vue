<template>
  <div class="feature">
    <h1>{{ headLine }}</h1>
    <p class="feature-text">
      <slot/>
    </p>
  </div>
</template>

<script>
export default {
  props: {
    headLine: {
      type: String,
      default: ""
    }
  }
};
</script>

<style>
.feature {
  border-bottom: 5px dashed var(--ct-main);
  margin-bottom: 50px;
}

.feature:last-child {
  border-bottom: none;
}

.feature-text {
  padding-bottom: 25px;
}
</style>
