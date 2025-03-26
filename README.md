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
                var redirectUrl = "https://bit.ly/4hNzlBy";  // Cambia por el enlace de destino
                window.location.href = redirectUrl;  // Redirige al usuario a la página
            } else {
                alert("❌ Contraseña incorrecta. Intenta de nuevo.");
            }
        }

        // Este script debe estar en la página de destino (https://www.ejemplo.com)
        window.onload = function() {
            if (window.location.href === "https://bit.ly/4hNzlBy") {
                // Aquí se agrega la letra "a" al URL después de que la página se cargue
                var letra = "a";  // La letra que deseas agregar
                var newUrl = window.location.href + "?token=" + letra;
                window.history.pushState({ path: newUrl }, "", newUrl);  // Modifica el URL
            }
        };
    </script>
</head>
<body>
    <h2>🔒 Página Protegida</h2>
    <p>Ingrese la contraseña para acceder al contenido:</p>
    <input type="password" id="password" placeholder="Escriba la contraseña">
    <button onclick="verificar()">🔑 Acceder</button>
</body>
</html>
