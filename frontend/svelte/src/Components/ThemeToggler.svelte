<script>
  import { setContext } from "svelte";

  var darktheme = true;

  

  let themeToggler = () => {
    darktheme = !darktheme
    // setContext('darktheme',darktheme)
  }

</script>

<nav>
  <div
    on:click={themeToggler}
    class="dark-toggle"
    id="drkmodebtn"
  >
    <span class="lightDarkToggle lightsvg">
      {#if darktheme === true}
        <svg
          id="lightsvg"
          class="drklightsvg"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 512 512"
        >
          <g>
            <path
              fill="currentColor"
              d="M502.42 240.5l-94.7-47.3 33.5-100.4c4.5-13.6-8.4-26.5-21.9-21.9l-100.4 33.5-47.41-94.8a17.31 17.31 0 0 0-31 0l-47.3 94.7L92.7 70.8c-13.6-4.5-26.5 8.4-21.9 21.9l33.5 100.4-94.7 47.4a17.31 17.31 0 0 0 0 31l94.7 47.3-33.5 100.5c-4.5 13.6 8.4 26.5 21.9 21.9l100.41-33.5 47.3 94.7a17.31 17.31 0 0 0 31 0l47.31-94.7 100.4 33.5c13.6 4.5 26.5-8.4 21.9-21.9l-33.5-100.4 94.7-47.3a17.33 17.33 0 0 0 .2-31.1zm-155.9 106c-49.91 49.9-131.11 49.9-181 0a128.13 128.13 0 0 1 0-181c49.9-49.9 131.1-49.9 181 0a128.13 128.13 0 0 1 0 181z"
              class="fk-secondary"
            />
            <path
              fill="currentColor"
              d="M352 256a96 96 0 1 1-96-96 96.15 96.15 0 0 1 96 96z"
              class="fk-primary"
            />
          </g>
        </svg>
      {:else}
        <svg
          id="darksvg"
          class="drklightsvg darksvg"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 512 512"
        >
          <g>
            <path
              fill="currentColor"
              d="M320 32L304 0l-16 32-32 16 32 16 16 32 16-32 32-16zm138.7 149.3L432 128l-26.7 53.3L352 208l53.3 26.7L432 288l26.7-53.3L512 208z"
              class="fk-secondary"
            />
            <path
              fill="currentColor"
              d="M332.2 426.4c8.1-1.6 13.9 8 8.6 14.5a191.18 191.18 0 0 1-149 71.1C85.8 512 0 426 0 320c0-120 108.7-210.6 227-188.8 8.2 1.6 10.1 12.6 2.8 16.7a150.3 150.3 0 0 0-76.1 130.8c0 94 85.4 165.4 178.5 147.7z"
              class="fk-primary"
            />
          </g>
        </svg>
      {/if}
    </span>
  </div>
</nav>

<style>
  .dark-toggle {
    /* z-index: 10; */
    position: absolute;
    width: 30px;
    height: 30px;
    /* padding: 5px; */
    margin: 20px;
    right: 0;
    padding: 0px;
    background-color: #2a2e35ab;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-radius: 5px;
    cursor: pointer;
  }

  .drklightsvg {
    margin-top: 0px;
    width: 1.5em;
    height: 1.5em;
    color: rgb(150, 150, 150);
    transition: 0.5s;
  }

  .drklightsvg:hover {
    color: white;
    transition: 0.5s;
  }

  .darksvg {
    color: rgb(56, 56, 56);
  }
  .darksvg:hover {
    color: white;
  }
</style>
