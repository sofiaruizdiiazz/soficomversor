# Conversor de Unidades

Este es un trabajo práctico simple hecho con **HTML, CSS y JavaScript**.  
El programa permite convertir:

- Centímetros a Metros  
- Metros a Kilómetros  

---

## 📌 Código del proyecto

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Conversor de Unidades</title>
  <style>
    body {
      background-color: #ADD8E6; /* Celeste */
      color: red; /* Letras rojas */
      font-family: Arial, sans-serif;
      padding: 20px;
    }

    h1 {
      text-align: center;
    }

    .converter {
      max-width: 400px;
      margin: 0 auto;
      padding: 20px;
      background-color: #ffffffaa;
      border-radius: 10px;
    }

    label, input, select, button {
      display: block;
      width: 100%;
      margin: 10px 0;
      font-size: 16px;
    }

    button {
      background-color: red;
      color: white;
      border: none;
      padding: 10px;
      cursor: pointer;
    }

    button:hover {
      background-color: darkred;
    }

    .resultado {
      margin-top: 15px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Conversor de Unidades</h1>

  <div class="converter">
    <label for="tipo">Selecciona la conversión:</label>
    <select id="tipo">
      <option value="cm-m">Centímetros a Metros</option>
      <option value="m-km">Metros a Kilómetros</option>
    </select>

    <label for="valor">Ingresa el valor:</label>
    <input type="number" id="valor" placeholder="Escribe un número">

    <button onclick="convertir()">Convertir</button>

    <div class="resultado" id="resultado"></div>
  </div>

  <script>
    function convertir() {
      const tipo = document.getElementById('tipo').value;
      const valor = parseFloat(document.getElementById('valor').value);
      const resultado = document.getElementById('resultado');

      if (isNaN(valor)) {
        resultado.textContent = 'Por favor, ingresa un número válido.';
        return;
      }

      let conversion = 0;
      let unidad = '';

      if (tipo === 'cm-m') {
        conversion = valor / 100;
        unidad = 'metros';
      } else if (tipo === 'm-km') {
        conversion = valor / 1000;
        unidad = 'kilómetros';
      }

      resultado.textContent = `Resultado: ${conversion} ${unidad}`;
    }
  </script>
</body>
</html>
```

---

## 🚀 Cómo usarlo
1. Descargar o clonar el repositorio.  
2. Abrir el archivo `index.html` en un navegador.  
3. Seleccionar el tipo de conversión.  
4. Ingresar el valor y hacer clic en **Convertir**.  

---

## 🔧 Tecnologías usadas
- HTML5  
- CSS3  
- JavaScript  

---

✍️ Proyecto realizado como trabajo práctico básico.
