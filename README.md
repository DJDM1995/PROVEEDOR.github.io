<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Acceso Protegido</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
        input, button { padding: 10px; margin: 10px; }
    </style>
    <script>
        function verificar() {
            var password = document.getElementById("password").value;
            
            if (password === "1234") {  // Cambia "1234" por tu contraseña
                window.location.href = "https://www.google.com"; // Cambia por el enlace al que quieres dirigir
            } else {
                alert("❌ Contraseña incorrecta. Intenta de nuevo.");
            }
        }

        // Evita copiar y pegar
        document.addEventListener("copy", (event) => event.preventDefault());
        document.addEventListener("paste", (event) => event.preventDefault());
    </script>
</head>
<body>
    <h2>🔒 Página Protegida</h2>
    <p>Ingrese la contraseña para acceder al contenido:</p>
    <input type="password" id="password" placeholder="Escriba la contraseña">
    <button onclick="verificar()">🔑 Acceder</button>
</body>
</html>
