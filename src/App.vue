<template>
  <div>
    <TheHeader />
    <div class="container">
      <router-view />
    </div>
  </div>
</template>
<script>
import TheHeader from "@/components/TheHeader";
export default {
  components: {
    TheHeader,
  },
};
</script>
<style>
</style>
