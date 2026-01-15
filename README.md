# 666
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <title>新增很多 67 + 擬真棒 + 跳轉</title>
  <style>
    body {
      font-family: sans-serif;
      margin: 20px;
    }
    #output {
      font-size: 20px;
      margin-top: 10px;
      color: #333;
      max-height: 300px;
      overflow-y: auto;
      border: 1px solid #ccc;
      padding: 10px;
      display: flex;
      flex-wrap: wrap;
    }
    .number {
      margin: 4px;
      display: inline-block;
    }
    #counter {
      margin-top: 10px;
      font-weight: bold;
    }
    #celebration {
      position: sticky;
      top: 0;
      background: yellow;
      font-size: 32px;
      color: red;
      padding: 10px;
      display: none;
      z-index: 10;
    }
  </style>
</head>
<body>
  <h2>每按一次就新增一個 67</h2>
  <button onclick="addNumber()">新增 67</button>
  <div id="counter">目前總數：0</div>
  <div id="celebration">🎉 擬真棒！🎉</div>
  <div id="output"></div>

  <script>
    let count = 0;

    function addNumber() {
      count++;
      const output = document.getElementById("output");
      const span = document.createElement("span");
      span.className = "number";
      span.textContent = "67";
      output.appendChild(span);

      document.getElementById("counter").textContent = "目前總數：" + count;

      const celebration = document.getElementById("celebration");
      if (count % 100 === 0) {
        celebration.style.display = "block";
      } else {
        celebration.style.display = "none";
      }

      if (count % 150 === 0) {
        // ✅ 在這裡填入你要跳轉的網址
        window.open("https://www.youtube.com/watch?v=dQw4w9WgXcQ", "_blank");
      }
    }
  </script>
</body>
</html>
