# Bungwa
Aplikasi bungwaandroid 

<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BUNG WA</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #101820;
      color: white;
      text-align: center;
      padding: 25px;
    }
    .container {
      max-width: 400px;
      margin: 50px auto;
      padding: 25px;
      background: #1d2b36;
      border-radius: 15px;
    }
    h1 { color: #25d366; }
    input, button {
      width: 100%;
      box-sizing: border-box;
      padding: 14px;
      margin-top: 12px;
      border: none;
      border-radius: 8px;
      font-size: 16px;
    }
    button {
      background: #25d366;
      color: white;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>BUNG WA</h1>
    <p>Masukkan nomor WhatsApp</p>
    <input id="nomor" type="tel" placeholder="Contoh: 628123456789">
    <button onclick="bukaWA()">BUKA WHATSAPP</button>
    <p id="pesan"></p>
  </div>

  <script>
    function bukaWA() {
      const nomor = document.getElementById("nomor").value
        .replace(/\D/g, "");

      if (!nomor) {
        document.getElementById("pesan").textContent =
          "Masukkan nomor terlebih dahulu!";
        return;
      }

      window.open("https://wa.me/" + nomor, "_blank");
    }
  </script>
</body>
</html>
