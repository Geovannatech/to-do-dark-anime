<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>To-Do</title>

  <!-- Fonte Fraktur -->
  <link href="https://fonts.googleapis.com/css2?family=UnifrakturCook:700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      min-height: 100vh;
      background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .container {
      background: #111;
      color: #fff;
      border: 2px solid #c77dff;
      box-shadow: 0 0 20px #9d4edd;
      padding: 20px;
      width: 320px;
      border-radius: 12px;
    }

    h1 {
      font-family: 'UnifrakturCook', cursive;
      text-align: center;
      margin-bottom: 15px;
      font-size: 32px;
    }

    .top {
      display: flex;
      gap: 6px;
    }

    input {
      flex: 1;
      padding: 8px;
      border-radius: 6px;
      border: none;
      outline: none;
    }

    button {
      padding: 8px 12px;
      border: none;
      border-radius: 6px;
      background: #9d4edd;
      color: #fff;
      cursor: pointer;
      font-weight: bold;
    }

    ul {
      list-style: none;
      margin-top: 10px;
    }

    li {
      background: #1e1e2e;
      padding: 6px;
      margin-bottom: 6px;
      border-radius: 6px;
      display: flex;
      justify-content: space-between;
      cursor: pointer;
    }

    li.done {
      text-decoration: line-through;
      opacity: 0.6;
    }
  </style>
</head>

<body>
  <div class="container">
    <h1>𝕿𝖔-𝕯𝖔</h1>

    <div class="top">
      <input id="taskInput" placeholder="Nova tarefa">
      <button onclick="addTask()">+</button>
    </div>

    <ul id="taskList"></ul>
  </div>

  <script>
    const input = document.getElementById("taskInput");
    const list = document.getElementById("taskList");

    function addTask() {
      if (input.value.trim() === "") return;

      const li = document.createElement("li");
      li.textContent = input.value;

      li.onclick = () => li.classList.toggle("done");

      list.appendChild(li);
      input.value = "";
    }
  </script>
</body>
</html>


http://127.0.0.1:5500/index.html
