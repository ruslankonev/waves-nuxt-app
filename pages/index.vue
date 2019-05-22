<template>
  <section class="container">
    <div>
      <h1 class="title">
        Mastering Web3 with Waves
      </h1>
      <div class="links">
        <a
          href="https://bitcoinnews.blog"
          target="_blank"
          rel="noopener"
          class="button--grey"
        >Read Web3</a>
        <a
          href="https://wavesplatform.com"
          target="_blank"
          rel="noopener"
          class="button--grey"
        >Connect with Waves</a>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #0a82ff;
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
