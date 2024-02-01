<template>
  <div>
    <div v-on:scroll="handleScroll" style="height: 200px; overflow-y: scroll;">
      <!-- Your content goes here -->
      <div style="height: 400px;"> <!-- Content to make the container scrollable -->
        <!-- Your scrollable content goes here -->
      </div>
    </div>
    <p>Scroll position: {{ scrollPosition }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      scrollPosition: 0
    };
  },
  methods: {
    handleScroll() {
      this.scrollPosition = event.target.scrollTop;
    }
  }
};
</script>
