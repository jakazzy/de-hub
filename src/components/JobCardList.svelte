<script>
  import { onMount } from "svelte";
  import JobCard from "./JobCard.svelte";
  import data from "../static-job-listings-master/data.js";

  let jobData = [];

  onMount(() => {
    jobData = data();
  });
</script>

{#each jobData as job (job.id)}
  <JobCard {job} />
{/each}
