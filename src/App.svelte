<script>
  import HowTo from "./HowTo.svelte";
  import Timer from "./Timer.svelte";
  let audio;
  function timerEnds(e) {
    audio.play();
    console.log(e);
  }
</script>

<style>
  h1,
  h3 {
    text-align: center;
  }
</style>

<h1>HandWashing App</h1>
<Timer on:end={timerEnds} />
<HowTo />

<h3>
  <a href="https://www.who.int/gpsc/clean_hands_protection/en/" target="_blank">
    Picture Source
  </a>

  <a
    href="https://freesound.org/people/metrostock99/sounds/345086/ "
    target="_blank">
    Sound Source
  </a>
</h3>

<!-- svelte-ignore a11y-media-has-caption -->
<audio bind:this={audio}>
  <source src="sound.wav" />
</audio>
