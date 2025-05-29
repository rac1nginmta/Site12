# Site12


Html:

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Página CSS3</title>
  <link rel="stylesheet" href="estilo.css" />
</head>
<body>
  <header>
    <h1>cs3 novo</h1>
  </header>

  <main class="container">
    <section class="card destaque">
      <h2>Flexbox e Grid</h2>
      <p>Layout responsivo com <code>display: flex</code> e <code>display: grid</code>.</p>
    </section>
    <section class="card">
      <h2>Transições</h2>
      <p>Suavidade com <code>transition</code> e <code>transform</code>.</p>
    </section>
    <section class="card">
      <h2>Aspect Ratio</h2>
      <p>Controle de proporção com <code>aspect-ratio</code>.</p>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 CSS3 Demo</p>
  </footer>
</body>
</html>






css:


* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


body {
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(to right, #f0f0f0, #e0e0e0);
  color: #333;
  line-height: 1.6;
}


header {
  background-color: #4a90e2;
  color: white;
  padding: 2rem;
  text-align: center;
  border-bottom-left-radius: 20px;
  border-bottom-right-radius: 20px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  padding: 2rem;
  content-visibility: auto;
  contain-intrinsic-size: 400px;
}


.card {
  background-color: white;
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  aspect-ratio: 4 / 3;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}


.destaque {
  background-color: rgba(74, 144, 226, 0.1);
  border-left: 5px solid #4a90e2;
}


footer {
  text-align: center;
  padding: 1rem;
  background-color: #f8f8f8;
  font-size: 0.9rem;
}


@media (max-width: 600px) {
  header h1 {
    font-size: 1.5rem;
  }

  .card {
    padding: 1rem;
  }
}


@supports (display: grid) {
  .container {
    display: grid;
  }
}
