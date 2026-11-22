<script lang="ts">
  import { page } from '$app/state';
</script>

<svelte:head>
  <title>Página no encontrada - renovando.uy</title>
  <meta name="description" content="La página que buscas no existe. Volvé al inicio de renovando.uy" />
</svelte:head>

<div class="container">
  <img src="/logo.jpeg" alt="renovando.uy" class="logo" />
  <h1>{page.status}</h1>
  <h2>Página no encontrada</h2>
  <p>La página que buscas no existe o fue movida. Volvé al inicio para encontrar lo que necesitás.</p>
  <a href="/" class="btn">Volver al inicio</a>
</div>

<style>
  .container {
    text-align: center;
    max-width: 600px;
    padding: 2rem;
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  }
  h1 {
    font-size: 4rem;
    margin: 0;
    font-weight: 300;
  }
  h2 {
    font-size: 1.5rem;
    margin: 1rem 0;
    font-weight: 400;
  }
  p {
    font-size: 1.1rem;
    margin: 2rem 0;
    opacity: 0.9;
  }
  .btn {
    display: inline-block;
    background: rgba(255, 255, 255, 0.2);
    color: white;
    padding: 1rem 2rem;
    text-decoration: none;
    border-radius: 8px;
    font-weight: 500;
    transition: background 0.3s ease;
    backdrop-filter: blur(10px);
  }
  .btn:hover {
    background: rgba(255, 255, 255, 0.3);
  }
  .logo {
    width: 80px;
    height: auto;
    margin-bottom: 2rem;
    border-radius: 8px;
  }
</style>
