<template>
  <section class="container">
    <div>
      <h1 class="title">Mastering Web3 with Waves</h1>
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
      <div class="waves">
        <a-button type="primary" @click="authFunc">Check Waves connect</a-button>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    methods: {
      authFunc() {
        const authData = { data: "Auth on my site" };
        if (WavesKeeper) {
          WavesKeeper.auth(authData)
            .then(auth => {
              console.log(auth); //displaying the result on the console
              /*...processing data */
            })
            .catch(error => {
              console.error(error); // displaying the result on the console
              /*...processing errors */
            });
        } else {
          alert("To Auth WavesKeeper should be installed.");
        }
      }
    }
  };
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

  .waves {
    margin-top: 2rem;
  }

  .title {
    font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
      "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #0a82ff;
    letter-spacing: 1px;
  }

  .links {
    padding-top: 1rem;
  }
</style>
