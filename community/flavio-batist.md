<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Verificador de URLs</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h1>Verificador de URLs</h1>
    <input type="text" id="urlInput" placeholder="Digite a URL aqui">
    <button onclick="verificarURL()">Verificar</button>
    <p id="resultado"></p>
  </div>
  <script src="script.js"></script>
</body>
</html>

body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f0f0f0;
  margin: 0;
}

.container {
  text-align: center;
  padding: 20px;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}

input {
  width: 300px;
  padding: 10px;
  margin-top: 10px;
}

button {
  padding: 10px 20px;
  margin-top: 10px;
  cursor: pointer;
}

p {
  margin-top: 20px;
  font-weight: bold;
}

function verificarURL() {
  const url = document.getElementById("urlInput").value;
  let resultado;

  if (url.startsWith("https://")) {
    resultado = "URL segura";
  } else if (url.startsWith("http://")) {
    resultado = "URL nao segura";
  } else {
    resultado = "Formato invalido";
  }

  document.getElementById("resultado").innerText = resultado;
}
