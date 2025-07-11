<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>حاسبة المجموع المعادل</title>
  <meta name="description" content="حاسبة إلكترونية لحساب المجموع المعادل بين النظام السعودي والثانوية العامة المصرية.">
  <meta name="keywords" content="حاسبة, المجموع المعادل, الثانوية العامة, السعودية, مصر, تحويل">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      text-align: center;
      padding: 30px;
      background-color: #f7f7f7;
    }
    h1 {
      margin-bottom: 10px;
    }
    .container {
      background: white;
      padding: 30px;
      border-radius: 8px;
      box-shadow: 0 0 10px #ccc;
      max-width: 400px;
      margin: auto;
    }
    input {
      padding: 10px;
      width: 90%;
      margin-bottom: 15px;
    }
    button {
      padding: 10px 20px;
      background-color: #2e8b57;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    .result {
      margin-top: 20px;
      font-size: 20px;
      color: #333;
    }
  </style>
</head>
<body>
  <h1>﷽</h1>
  <div class="container">
    <h2>حاسبة المجموع المعادل</h2>
    <input type="number" id="school" placeholder="درجة المدرسة (%)">
    <input type="number" id="qdrat" placeholder="درجة القدرات (%)">
    <button onclick="calculate()">احسب المجموع المعادل</button>
    <div class="result" id="result"></div>
  </div>

  <script>
    function calculate() {
      const school = parseFloat(document.getElementById("school").value);
      const qdrat = parseFloat(document.getElementById("qdrat").value);

      if (isNaN(school) || isNaN(qdrat)) {
        document.getElementById("result").innerText = "من فضلك أدخل القيم الصحيحة.";
        return;
      }

      const total = (school * 0.7) + (qdrat * 0.3);
      const masrEquivalent = (total / 100) * 410;

      document.getElementById("result").innerText = 
        `المجموع المعادل للثانوية العامة: ${masrEquivalent.toFixed(2)} من 410`;
    }
  </script>
</body>
</html>
