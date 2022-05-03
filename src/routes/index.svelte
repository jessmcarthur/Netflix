<script>
  import Header from '$components/Header.svelte'
  import Nav from '$components/Nav.svelte'
  
</script>


<Header />

<Nav />

<main>
  <h2>Netflix</h2>

  <p>
    Netflix said that “Bridgerton” was watched by 82 million member households
    globally in its first 28 days (it debuted on Christmas), making it Netflix’s
    biggest original series of all time. Netflix counts a view if an account
    watches at least two minutes of a show or movie, so while the metric doesn’t
    account for how many users watched the entire series, it does provide a good
    idea of how many were interested in it.
  </p>

  <p>Click the links above to explore the top 3 biggest Netflix shows.</p>
</main>



<style>
  /* LAYOUT */
  :global(Header) { grid-area: h; }
  :global(Nav)    { grid-area: n; }
  :global(main)   { grid-area: m; }
  

  :global(#svelte) {
    display: grid;
    grid: " h   n   " auto
          " m   m   " auto
          
          / 3fr 1fr ;
  }

  /* GLOBAL STYLES */
  :global(main) {
    padding: 2em 10em;
  }

  :global(h2) {
    font-size: 1.5em;
    font-weight: bold;
    margin-bottom: 1em;
  }
</style>