<!doctype html>
<html lang="uk">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>❤️ Любовний лічильник</title>
  <style>
    body { font-family: system-ui, Arial, sans-serif; padding: 24px; max-width: 520px; margin: 0 auto; }
    h1 { margin-bottom: 8px; }
    .box { display: flex; gap: 10px; margin-top: 14px; }
    input { flex: 1; padding: 10px; font-size: 16px; }
    button { padding: 10px 14px; font-size: 16px; cursor: pointer; }
    #result { margin-top: 16px; font-size: 18px; font-weight: 600; }
    small { color: #666; }
  </style>
</head>
<body>
  <h1>Введи число ❤️</h1>
  <p>Введи число, на скільки сильно ти мене любиш:</p>

  <div class="box">
    <input id="loveNumber" type="number" placeholder="Наприклад: 10" />
    <button id="btn">Показати</button>
  </div>

  <div id="result"></div>

  <script>
    const input = document.getElementById("loveNumber");
    const result = document.getElementById("result");
    const btn = document.getElementById("btn");

    function showLove() {
      const value = Number(input.value);

      if (!Number.isFinite(value)) {
        result.textContent = "Введи, будь ласка, число 🙂";
        return;
      }

      result.textContent = `А я тебе люблю на ${value + 1} ❤️`;
    }

    btn.addEventListener("click", showLove);
    input.addEventListener("keydown", (e) => {
      if (e.key === "Enter") showLove();
    });
  </script>
</body>
</html>
