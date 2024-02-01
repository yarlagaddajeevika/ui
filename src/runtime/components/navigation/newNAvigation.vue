<template>
  <div>
    <div :style="{ backgroundColor: backgroundColor }" class="scroll-container">
      <!-- Your content goes here -->
      <div style="height: 400px;">
        <!-- Your scrollable content goes here -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      backgroundColor: 'transparent'
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      // Change background color based on scroll position
      const scrollPosition = window.scrollY;

      if (scrollPosition > 100) {
        this.backgroundColor = 'lightblue';
      } else {
        this.backgroundColor = 'transparent';
      }
    }
  }
};
</script>

<style>
.scroll-container {
  transition: background-color 0.5s ease;
}
</style>
