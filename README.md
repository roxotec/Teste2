# Teste2

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Agendamento de Barbearia</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <h1>Agendamento de Barbearia</h1>
    <label for="name">Nome:</label>
    <input type="text" id="name" required>
    <label for="service">Serviço:</label>
    <select id="service" required>
      <option value="corte">Corte de Cabelo</option>
      <option value="barba">Barba</option>
      <option value="corte_barba">Corte e Barba</option>
    </select>
    <label for="date">Data:</label>
    <input type="date" id="date" required>
    <label for="time">Horário:</label>
    <input type="time" id="time" required>
    <button onclick="agendar()">Agendar</button>
  </div>

  <script src="script.js"></script>
</body>
</html>

body {
  font-family: Arial, sans-serif;
}

.container {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input, select {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
}

button {
  background-color: #007BFF;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

function agendar() {
  const name = document.getElementById("name").value;
  const service = document.getElementById("service").value;
  const date = document.getElementById("date").value;
  const time = document.getElementById("time").value;

  // Aqui você pode implementar a lógica para armazenar os dados do agendamento,
  // por exemplo, enviando para um servidor ou armazenando em um banco de dados.

  alert(`Agendamento realizado:\nNome: ${name}\nServiço: ${service}\nData: ${date}\nHorário: ${time}`);
}
