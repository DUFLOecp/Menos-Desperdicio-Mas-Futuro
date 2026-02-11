<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Menos Desperdicio, Más Futuro</title>

  <!-- Fuente moderna -->
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;800&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      font-family: 'Montserrat', sans-serif;
      background: #f4f6f5;
      color: #2c2c2c;
    }

    /* Encabezado */
    header {
      background: #ffffff;
      border-bottom: 4px solid #2e7d32;
      padding: 20px 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    header img {
      height: 55px;
    }

    h1 {
      font-size: 32px;
      font-weight: 800;
      color: #2e7d32;
      margin: 0;
      letter-spacing: 1px;
    }

    /* Contenedor */
    .container {
      max-width: 900px;
      margin: 50px auto;
      padding: 0 20px;
    }

    .card {
      background: #ffffff;
      border-radius: 14px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.08);
      padding: 35px;
    }

    .card h2 {
      color: #c62828;
      font-size: 22px;
      margin-bottom: 10px;
      font-weight: 700;
    }

    .card p {
      font-size: 14px;
      color: #555;
      margin-bottom: 25px;
    }

    label {
      font-weight: 600;
      font-size: 14px;
    }

    input {
      width: 100%;
      padding: 14px;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 16px;
      margin-top: 8px;
    }

    button {
      margin-top: 25px;
      width: 100%;
      background: #2e7d32;
      color: white;
      border: none;
      padding: 14px;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
      font-weight: 600;
    }

    button:hover {
      background: #1b5e20;
    }

    .result {
      margin-top: 30px;
      background: #f1f8f4;
      border-radius: 10px;
      padding: 20px;
      font-size: 14px;
    }

    .result div {
      margin-bottom: 10px;
    }

    .alert {
      color: #c62828;
      font-weight: 600;
      margin-top: 15px;
      text-align: center;
    }

    footer {
      text-align: center;
      margin: 40px 0 20px;
      font-size: 12px;
      color: #777;
    }
  </style>
</head>

<body>

<header>
  <img src="ecopetrol.png" alt="Ecopetrol">
  <h1>MENOS DESPERDICIO, MÁS FUTURO</h1>
  <img src="duflo.png" alt="Duflo">
</header>

<div class="container">
  <div class="card">
    <h2>Impacto del Desperdicio de Alimentos</h2>
    <p>
      Cada kilogramo de alimento desperdiciado representa un uso innecesario de agua,
      energía y genera emisiones evitables.
    </p>

    <label>Peso del alimento desechado (kg)</label>
    <input type="number" id="kg" placeholder="Ejemplo: 1.5" min="0" step="0.1">

    <button onclick="calcular()">Calcular impacto</button>

    <div class="result" id="resultado" style="display:none;">
      <div>💧 <b>Agua utilizada:</b> <span id="agua"></span> litros</div>
      <div>⚡ <b>Energía utilizada:</b> <span id="energia"></span> kWh</div>
      <div>🌫️ <b>Emisiones de CO₂:</b> <span id="co2"></span> kg</div>
      <div class="alert">
        Reducir el desperdicio es una acción directa contra el cambio climático.
      </div>
    </div>
  </div>
</div>

<footer>
  Campaña ambiental · Uso educativo y corporativo
</footer>

<script>
  function calcular() {
    const kg = parseFloat(document.getElementById('kg').value);

    if (!kg || kg <= 0) {
      alert("Por favor ingresa un valor válido.");
      return;
    }

    const agua = kg * 1300;
    const energia = kg * 4;
    const co2 = kg * 2.5;

    document.getElementById('agua').innerText = agua.toFixed(0);
    document.getElementById('energia').innerText = energia.toFixed(2);
    document.getElementById('co2').innerText = co2.toFixed(2);

    document.getElementById('resultado').style.display = 'block';
  }
</script>

</body>
</html>
