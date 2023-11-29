<script lang="ts">
  import { Canvas } from '@threlte/core';
  import Scene from './Scene.svelte';

  let nextScreen: () => void;
  const handleClick = () => {
    nextScreen();
  }

</script>

<Canvas>
  <Scene bind:nextScreen={nextScreen}/>
</Canvas>


  <!-- Example of changing the texture based on an event -->
  <button on:click={handleClick} style="position: absolute; top: 0;">
    Change Texture
  </button>
  