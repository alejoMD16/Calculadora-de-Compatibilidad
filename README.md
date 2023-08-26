# Calculadora-de-Compatibilidad
<!DOCTYPE html>
<html>
<head>
    <title>CalculadoraDeCompatibilidad</title>
</head>
<body>
    <h1>Calculadora de Compatibilidad</h1>
    <form id="compatibilidadForm">
        <label for="nombre1">Ingresar nombre 1:</label>
        <input type="text" id="nombre1" name="nombre1"><br><br>
        <label for="nombre2">Ingresar nombre 2:</label>
        <input type="text" id="nombre2" name="nombre2"><br><br>
        <button type="button" onclick="calcularCompatibilidad()">Calcular Compatibilidad</button>
    </form>
    <p id="resultado"></p>

    <script>
        function calcularCompatibilidad() {
            var m = document.getElementById('nombre1').value;
            var x = document.getElementById('nombre2').value;
            var n = Math.floor(Math.random() * 101);

            var mensaje = "";

            if (n < 5) {
                mensaje = "Ni una amistad funcionaría entre ustedes";
            } else if (n >= 5 && n < 20) {
                mensaje = "Deberían ser solo amigos";
            } else if (n >= 20 && n < 40) {
                mensaje = "Buenos amigos";
            } else if (n >= 40 && n < 65) {
                mensaje = "Podrían darse una oportunidad";
            } else if (n >= 65 && n < 80) {
                mensaje = "Serían una excelente pareja";
            } else if (n >= 80 && n < 85) {
                mensaje = "Son la mejor pareja que he visto";
            } else if (n >= 85 && n < 99) {
                mensaje = "Cásense de una vez";
            } else if (n == 100) {
                mensaje = "Están destinados a estar juntos por siempre";
            }

            var resultadoElemento = document.getElementById('resultado');
            resultadoElemento.textContent = "Su porcentaje de compatibilidades es: " + n + ". " + mensaje;
        }
    </script>
</body>
</html>
