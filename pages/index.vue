<template>
    <div>
    <header>
    <nav class="nav">
    <div class="logo">RA</div>
    <div class="nav-link">Experience</div>
    <div class="nav-link">Contact</div>
    </nav>
    </header>
      <main class="main">
      <div class="bio">
        <!-- <div class="bio-name">
        Robert Arteaga
        </div> -->
        <div class="bio-summary">
         Just a Creative Frontend Developer & Designer.
        </div>
        <div class="bio-summary-2">
         Architecting Modern UI's That Empower Companies
        </div>
      </div>
      </main>
      <div class="designer-container">
        <div class="designer">Designer</div>
      </div>

      <div class="developer-container">
        <div class="year">2020</div>
        <div class="developer">Developer</div>
      </div>


      <!-- <div class="work-availibility">
        <div class="triangle-corner">
        <span class="triangle-corner-span">Available</span>
        <span class="triangle-corner-span">For</span>
        <span class="triangle-corner-span">Hire</span>
        </div>
      </div> -->

      <div class="circle-follow" ref="cursor"></div>

    </div>
</template>

<script>
import Vue from 'vue'
  import { gsap } from 'gsap';
export default {
  mounted() {
    const {cursor} = this.$refs
    const cursorTimeline = gsap.timeline()

    window.addEventListener("mousemove", e => {
      if (getComputedStyle(e.target).backgroundColor === "rgb(24,24,24)") {
        cursorTimeline.to(cursor, 0.35, {
          x: e.clientX,
          y: e.clientY,
          scale: 1.5,
          border: "2px solid #ffffff",
        })
      } else {
        cursorTimeline.to(cursor, 0.25, {
          x: e.clientX,
          y: e.clientY,
          scale: 1,
          border: "2px solid black",
        })
      }
  })
  }
}
</script>

<style>
.bio {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  line-height: 1.8;
}
.bio-name {
  font-size: 1em;
  text-transform: lowercase;
}

.bio-summary {
  font-size: 1.8em;
}
.bio-summary-2 {
  font-size: 1.1em;
}
.nav-link {
    text-transform: uppercase;
    letter-spacing: 1px;
    padding-right: 2rem;
    font-size: 0.9em;
  }

.nav{
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

body {
  font-family: 'Playfair Display', serif;
  max-height: 100vh;
  overflow: hidden;
  background: #fbfbfb;
    -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-weight: normal;
  font-kerning: normal;
  -moz-font-feature-settings: "kern", "liga", "clig", "calt";
  -ms-font-feature-settings: "kern", "liga", "clig", "calt";
  -webkit-font-feature-settings: "kern", "liga", "clig", "calt";
  font-feature-settings: "kern", "liga", "clig", "calt";
}

.main {
  padding-top: calc(10vmax - 4rem);
  padding-bottom: 10vmax;
  min-height: 100vh;
  position: relative;
  display: flex;
  position: relative;
  justify-content: center;
  align-items: center;
}

.work-availibility {
  position: absolute;
  right: -10rem;
  bottom: -10rem;
  width: 20rem;
  height: 20rem;
}

.triangle-corner {

  border: black 1px solid;
  height: 20rem;
  width: 20rem;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  text-transform: lowercase;

}
.triangle-corner-span {
  margin-right: 7.5rem;
  margin-bottom: 7.5rem;
}

header {
  width: 50vw;
  height: 4rem;
  padding-left: 3rem;
  padding-top: 1rem;

}
.logo {
  font-size: 2em;
  padding-right: 3rem;
}
.developer-container {
  position: absolute;
  left: 3rem;
  bottom: -3vmax;
  width: 50vmax;
}

.designer-container {
  position: absolute;
  right: 3rem;
  top: -3vmax;
  width: 50vmax;
}

.year {
  text-orientation: sideways-right;
  writing-mode: vertical-rl;
  font-size: 2vmax;
  font-weight: 400;
  color: rgb(24,24,24);
}

.designer {
  font-size: 10vmax;
  font-weight: inherit;
  line-height: 1;
  text-transform: uppercase;
  text-align: right;
  color: rgba(24,24,24);
}

.developer {
  font-size: 10vmax;
  font-weight: inherit;
  line-height: 1;
  text-transform: uppercase;
  text-align: left;
  color: rgba(24,24,24);
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

.circle-follow {
  position: fixed;
  border: 2px solid #222222;
  width: 36px;
  height: 36px;
  left: -21px;
  top: -21px;
  border-radius: 100%;
  z-index: 1;
  user-select: none;
  pointer-events: none;
  z-index: 10000;
  transform: scale(1);
}
</style>
