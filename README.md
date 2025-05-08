<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Tap Millonario</title>
  <style>
    body {
      margin: 0;
      font-family: sans-serif;
      background-color: #222;
      color: white;
      text-align: center;
      user-select: none;
    }
    .contenedor {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    h1 {
      font-size: 2.5rem;
    }
    #puntos {
      font-size: 3rem;
      margin-top: 20px;
      color: #00ff88;
    }
    .pantalla {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
    }
  </style>
</head>
<body>
  <div class="contenedor">
    <h1>¡Toca o haz clic para sumar puntos!</h1>
    <div id="puntos">0</div>
    <div class="pantalla" onclick="sumarPunto()"></div>
  </div>

  <script>
    let puntos = 0;
    const objetivo = 1000000000;
    const puntosTexto = document.getElementById("puntos");

    function sumarPunto() {
      puntos++;
      puntosTexto.textContent = puntos.toLocaleString("es-ES");
      if (puntos >= objetivo) {
        alert("¡Llegaste a 1.000.000.000 puntos!");
      }
    }
  </script>
</body>
</html>{
  "name": "ganador-tap",
  "version": "1.0.0",
  "main": "servidor.js",
  "type": "module",
  "scripts": {
    "start": "node servidor.js"
  },
  "dependencies": {
    "express": "^4.18.2",
    "cors": "^2.8.5"
  }
}node_modules
ganador.json
