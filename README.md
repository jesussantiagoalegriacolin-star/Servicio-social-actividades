# Servicio-social-actividades
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Servicios Sociales Registro</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.7/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.7/dist/js/bootstrap.bundle.min.js"></script>
  <style>
    body {
      padding: 20px;
    }
    h1 {
      color: #0d6efd; /* Azul Bootstrap */
    }
    .blue-row {
      background-color: #cce5ff;
    }
    .pink-row {
      background-color: #f8d7da;
    }
    .red-row {
      background-color: #f5c6cb;
    }
    .imagen {
      max-width: 100%;
      height: auto;
      border: 2px solid #333;
      border-radius: 10px;
      margin-top: 20px;
    }
    input[type="file"] {
      margin-top: 20px;
      padding: 10px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    input[type="file"]:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>

  <h1>¡Bienvenidos al registro de actividades de servicios sociales!</h1>

  <div class="mb-3">
    <label for="email" class="form-label">Añade una cuenta</label>
    <input type="email" class="form-control" id="email" placeholder="name@example.com">
  </div>

  <div class="mb-3">
    <label for="info" class="form-label">Nombre completo y lugar de servicio donde entregas tus actividades</label>
    <textarea class="form-control" id="info" rows="3"></textarea>
  </div>

  <table class="table table-bordered">
    <thead class="table-primary">
      <tr>
        <th>#</th>
        <th>Tema</th>
        <th>Septiembre 2025</th>
        <th>Octubre 2025</th>
      </tr>
    </thead>
    <tbody>
      <tr class="blue-row">
        <th scope="row">1</th>
        <td>Domina el tema y practica en voz alta</td>
        <td>Miércoles 3 y Jueves 4</td>
        <td>Hasta la semana 5</td>
      </tr>
      <tr class="pink-row">
        <th scope="row">2</th>
        <td>Visualiza el éxito y respiración profunda</td>
        <td>Miércoles 10 y Jueves 11</td>
        <td>Hasta la semana 5</td>
      </tr>
      <tr class="red-row">
        <th scope="row">3</th>
        <td>Adopta una postura de poder y canaliza tu energía</td>
        <td>Miércoles 17 y Jueves 18</td>
        <td>Hasta semana 5</td>
      </tr>
      <tr class="blue-row">
        <th scope="row">4</th>
        <td>Haz pausas y varía tu ritmo</td>
        <td>Miércoles 24 y Jueves 25</td>
        <td>Hasta semana 5</td>
      </tr>
      <tr class="pink-row">
        <th scope="row">5</th>
        <td>Utiliza notas clave y establece contacto visual</td>
        <td>Empieza con octubre</td>
        <td>Miércoles 1 y Jueves 2</td>
      </tr>
      <tr class="red-row">
        <th scope="row">6</th>
        <td>Sonríe y sé honesto contigo mismo</td>
        <td>Empieza octubre</td>
        <td>Miércoles 8 y Jueves 9</td>
      </tr>
      <tr class="blue-row">
        <th scope="row">7</th>
        <td>Capacitación e inicia siguiente etapa</td>
        <td>Continúa octubre</td>
        <td>Miércoles 15 y Jueves 16</td>
      </tr>
    </tbody>
  </table>

  <h2>Sube aquí tus actividades</h2>
  <input type="file" accept="image/png, image/jpeg" id="imagenInput">
  <img id="imagenMostrada" class="imagen" src="" alt="Imagen seleccionada" style="display: none;">

  <p class="mt-4"><strong>Nota:</strong> La hora límite para la entrega de sus actividades es hasta las <strong>6:00pm</strong>. En caso de que se entreguen después del tiempo límite, su actividad se tomará como entrega extemporánea.  
  <br>Si desean expandir su entrega a más tiempo, solicítenlo con la Lic. Laura Díaz Bernal.</p>

  <script>
    const imagenInput = document.getElementById('imagenInput');
    const imagenMostrada = document.getElementById('imagenMostrada');

    imagenInput.addEventListener('change', function(event) {
      const archivo = event.target.files[0];
      if (archivo) {
        const url = URL.createObjectURL(archivo);
        imagenMostrada.src = url;
        imagenMostrada.style.display = 'block';
      } else {
        imagenMostrada.style.display = 'none';
      }
    });
  </script>

</body>
</html>
