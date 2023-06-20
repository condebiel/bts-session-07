<template>
  <div 
		v-editable="blok"
		class="hero-banner"
	>
    <img :src="blok.imageUrl" :alt="blok.text" class="w-full h-auto">
    <div class="overlay"></div>
    <div class="content">
      <p>{{ blok.text }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({ blok: Object })
</script>

<style scoped>
.hero-banner {
  position: relative;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #fff;
	font-size: 2rem;
}
</style>
