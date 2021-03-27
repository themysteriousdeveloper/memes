<script>
  import { onMount } from 'svelte';
  import { Link } from 'svelte-routing';

//memes.author

  // API URL
  var apiBaseurl = 'https://meme-api.herokuapp.com/gimme';
  let memes = [];

  onMount(async () => {
    memes = [];
    const result = await fetch(apiBaseurl); // Calls the api with a "fetch" method in a async enviroment
    memes = await result.json(); // gets the results in a varible
    console.log(memes)
  })

  async function updateMeme() {
    const result = await fetch(apiBaseurl); // Calls the api with a "fetch" method in a async enviroment
    memes = await result.json(); // gets the results in a varible
  }

</script>

<h1>Memes &nbsp; &nbsp; <a href="#" on:click={updateMeme}><i class="material-icons">refresh</i></a></h1>


<div class="row">
  {#if memes.length === 0}
    <div class="progress">
      <div class="indeterminate"></div>
    </div>
  {:else}
      <link rel="shortcut icon" href={memes.preview[0]}>
      <div class="col cyan">
        <div class="card scale-transition scale-in">
          <div class="card-content">
              <span class="card-title"><a href={memes.postLink}>{memes.title}</a></span>
              <p>by {memes.author}</p>
              <p>r/{memes.subreddit}</p>
          </div>
          <div class="card-image waves-effect waves-block waves-light">
            <img src="{memes.url}" alt={memes.preview[0]}>
          </div>
        </div>
      </div>
  {/if}
</div>
<div class="spacer"></div>

<style>
  .spacer {
    height: 40rem;
  }
</style>
