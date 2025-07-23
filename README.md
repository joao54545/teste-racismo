<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Você é Racista?</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f9f9f9;
      color: #333;
      padding: 2rem;
      max-width: 700px;
      margin: auto;
    }

    h1 {
      text-align: center;
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }

    .question {
      margin-bottom: 1.2rem;
      padding: 1rem;
      background-color: #fff;
      border: 1px solid #ddd;
      border-radius: 10px;
    }

    label {
      display: block;
      margin-bottom: 0.5rem;
    }

    button {
      display: block;
      margin: 2rem auto;
      padding: 1rem 2rem;
      font-size: 1.1rem;
      background-color: #4caf50;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    button:hover {
      background-color: #45a049;
    }

    #resultado {
      text-align: center;
      font-size: 1.5rem;
      margin-top: 2rem;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Você é Racista? 🤨</h1>

  <form id="quizForm">
    <div class="question">
      <label><input type="checkbox" name="resposta" value="1"> "Não sou racista, até tenho amigos que são..."</label>
      <label><input type="checkbox" name="resposta" value="1"> Já disse "é só uma piada, relaxa"</label>
      <label><input type="checkbox" name="resposta" value="1"> Acha que racismo não existe mais hoje em dia</label>
    </div>

    <div class="question">
      <label><input type="checkbox" name="resposta" value="1"> Usa o termo "minorias mimimi"</label>
      <label><input type="checkbox" name="resposta" value="1"> Já reclamou de cotas em universidades</label>
    </div>

    <div class="question">
      <label><input type="checkbox" name="resposta" value="1"> Já confundiu cultura com crime (ex: funk = bandido)</label>
      <label><input type="checkbox" name="resposta" value="1"> Acha que "racismo reverso" é real</label>
    </div>

    <button type="button" onclick="verResultado()">Ver meu resultado</button>
  </form>

  <div id="resultado"></div>

  <script>
    function verResultado() {
      const respostas = document.querySelectorAll('input[name="resposta"]:checked');
      const pontos = respostas.length;
      let resultadoTexto = "";

      if (pontos <= 2) {
        resultadoTexto = "Você passou no teste (por enquanto...) 👀";
      } else if (pontos <= 4) {
        resultadoTexto = "Talvez seja só ignorância... ou não 🤨";
      } else {
        resultadoTexto = "Parabéns, você é o orgulho do tio do zap. 🧓📲🚩";
      }

      document.getElementById("resultado").innerText = resultadoTexto;
    }
  </script>
</body>
</html>
