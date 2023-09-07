<script lang="ts">
  let debug = "";

  async function hit_debug() {
    try {
      await navigator.mediaDevices.enumerateDevices();
      debug = "worked without issue";
    } catch (e) {
      console.error("Error:", e);
      debug = e;
    }
  }
</script>

<main class="container">
  <button on:click={hit_debug}>Push to try navigator</button>

  <p>
    {debug}
  </p>
</main>

<style>
  .logo.vite:hover {
    filter: drop-shadow(0 0 2em #747bff);
  }

  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00);
  }
</style>
