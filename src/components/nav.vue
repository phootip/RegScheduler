<template>
  <nav class="navbar is-fixed-top">
    <div class="container">
      <div class="navbar-brand">
        <router-link to="/" class="navbar-item is-size-4">
          reg-scheduler
        </router-link>
        <div class="navbar-burger" :class="{ 'is-active': isMenuActive }" @click="toggleMenu">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
      <div class="navbar-menu" :class="{ 'is-active': isMenuActive }">
        <router-link to="/" class="navbar-item">
          Schedule
        </router-link>
        <a class="navbar-item">
          Summary
        </a>
        <div class="navbar-end">
          <router-link to="/about" class="navbar-item">
            About
          </router-link>
          <a href="https://github.com/phootip/reg-scheduler" target="_blank" class="navbar-item is-hidden-touch"
          aria-label="GitHub Repository" title="GitHub Repository">
            <b-icon
              icon="github-circle"
            />
          </a>
          <a href="https://github.com/phootip/reg-scheduler" target="_blank" class="navbar-item is-hidden-desktop">
            GitHub repository
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Nav',
  data() {
    return {
      isMenuActive: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuActive = !this.isMenuActive;
    },
  },
};
</script>

