<template>
    
    <div class="profession-year-container">
    <div class="year">2020</div>
    <div class="profession">Dev Frontend</div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  components: {
  }
})
</script>

<style>

body {
  font-family: 'Playfair Display', serif;
  max-height: 100vh;
  overflow: hidden;
}

.profession-year-container {
  position: absolute;
  left: 3rem;
  bottom: -3rem;
  width: 50vmax;
}

.year {
  text-orientation: sideways-right;
  writing-mode: vertical-rl;
  font-size: 2vmax;
  font-weight: 500;
  color: rgba(24,24,24,0.8);
}

.profession {
  font-size: 12vmax;
  font-weight: 400;
  line-height: 1;
  text-transform: uppercase;
  text-align: left;
  color: rgba(24,24,24,0.8);
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
