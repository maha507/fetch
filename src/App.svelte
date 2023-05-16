<script>
  import { onMount } from "svelte";
  import Grid from "gridjs-svelte"
  const endpoint = "https://jsonplaceholder.typicode.com/posts";
  let posts = [];

  onMount(async function () {
    const response = await fetch(endpoint);
    const data = await response.json();
    console.log(data);
  });
  
  export let name;
</script>

<main>
  <h1>click the data</h1>
  <p>Visit the <a href="https://api.recruitly.io/api/job?apiKey=TEST64518616D4CF145D4E20BD47169EA7229BA3">data</a> for more details.</p>

  {#each posts as article}
    <div>
      <p>{article.title}</p>
    </div>
  {/each}
</main>
