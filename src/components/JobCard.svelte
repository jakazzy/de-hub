<script>
  export let job = {};
</script>

<div class="job-card">
  <div class="job-card__logo">
    <div class="logo">
      <p>{job.company}</p>
    </div>
  </div>

  <div class="job-card__Details">
    <div class="job-card__Details-header">
      <p class="company-name" style="margin-top: 20px;">{job.company}</p>
      <p class="new-tag">New!</p>
      <p class="featured-tag">Featured</p>
    </div>

    <div class="job-card__Details-name">
      <p>{job.position}</p>
    </div>

    <div class="job-card__Details-footer">
      <p class="posting-date">{job.postedAt}</p>
      <p class="job-state">{job.contract}</p>
      <p class="job-location">{job.location}</p>
    </div>
  </div>
  <div class="job-card__tags">
    <p class="tag">{job.role}</p>
    <p class="tag">{job.level}</p>
    {#each job.languages as lang}
      <p class="tag">{lang}</p>
    {/each}
    {#each job.tools as tool}
      <p class="tag">{tool}</p>
    {/each}
  </div>
</div>

<style>
  .job-card {
    width: 60%;
    height: 13rem;
    margin: 3rem auto;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    display: flex;
    flex-wrap: wrap;
    border-left: 5px solid rgba(94, 164, 165, 255);
    border-radius: 5px;
    background-color: white;
  }

  .job-card__logo {
    width: 20%;
    position: relative;
  }

  .job-card__Details {
    width: 40%;
  }

  .job-card__tags {
    width: 35%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    width: 7rem;
    height: 7rem;
    text-align: center;
    border-radius: 50%;
    background-color: #000;
    color: #fff;
    position: absolute;
    top: 50%;
    left: 20%;
    transform: translateY(-50%);
    display: flex;
    justify-content: center;
    align-content: center;
    flex-direction: column;
  }

  .job-card__Details-header {
    display: flex;
    justify-content: space-between;
    width: 65%;
  }

  .new-tag {
    background-color: #7db5b4;
    width: 3rem;
  }
  .featured-tag {
    background-color: #000;
    width: 5rem;
  }

  .new-tag,
  .featured-tag {
    text-align: center;
    color: white;
    padding: 0.3rem;
    border-radius: 20px;
  }

  .job-card__Details-name {
    font-weight: 500;
    font-size: 1.3rem;
  }

  .job-card__Details-footer {
    display: flex;
    justify-content: space-between;
    width: 65%;
    color: #8e9696;
  }

  .tag {
    background-color: rgba(219, 232, 232, 255);
    color: #65b9ba;
    height: 1rem;
    padding: 0.3rem;
    border-radius: 8px;
    text-align: center;
  }

  @media only screen and (max-width: 768px) {
    .job-card {
      width: 90%;
      height: 17rem;
    }

    .logo {
      width: 5rem;
      height: 5rem;
      text-align: center;
      border-radius: 50%;
      background-color: #000;
      color: #fff;
      position: absolute;
      top: -6%;
      left: -36%;
      transform: translateY(-50%);
      display: flex;
      justify-content: center;
      align-content: center;
      flex-direction: column;
    }

    .job-card__Details {
      width: 70%;
    }

    .job-card__Details-header,
    .job-card__Details-footer,
    .job-card__tags {
      width: 100%;
    }
  }
</style>
