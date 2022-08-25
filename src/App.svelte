<script>
  import Router, {location, link} from 'svelte-spa-router';
  import About from './lib/About.svelte';
  import Home from './lib/Home.svelte';
  import Projects from './lib/Projects.svelte';
</script>
<nav class="navbar navbar-expand-sm bg-dark navbar-dark">
  <div class="container-fluid ">
    <a class="navbar-brand" href="/">Logo</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#collapsibleNavbar">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="justify-content-end collapse navbar-collapse " id="collapsibleNavbar">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link" href="/">Anasayfa</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/#/about">Hakkımda</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/#/projects">Projeler</a>
        </li>
      </ul>
    </div>
  </div>
</nav>

<Router routes={{
	'/': Home,
	'/about': About,
  '/projects': Projects,
}} />

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
    :global(.card-img-top){
    border-top-left-radius:4px;
    border-top-right-radius:4px;
    border-bottom-left-radius:0px;
    border-bottom-right-radius:0px;
    height:25vh;
    border:#dededf 1px solid;
  }
  :global(.card){
    width:100%
  }
</style>
