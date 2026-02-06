<!DOCTYPE html><html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Spa Relajarte</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background-color: #f4f4f4;
    }
    header {
      background: #cd7bd6;
      color: #fff;
      padding: 15px;
      text-align: center;
    }
    nav {
      background: #df7cc7;
      display: flex;
      justify-content: center;
      gap: 20px;
      padding: 10px;
    }
    nav a {
      color: #fff;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      padding: 30px;
      display: none;
    }
    section.active {
      display: block;
    }
    .card {
      background: #fff;
      padding: 20px;
      border-radius: 8px;
      max-width: 900px;
      margin: auto;
    }
    .login-box {
      max-width: 400px;
      margin: 60px auto;
      background: #fff;
      padding: 30px;
      border-radius: 8px;
    }
    input, textarea, button {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
    }
    button {
      background: #e491ec;
      color: #fff;
      border: none;
      cursor: pointer;
    }
    button:hover {
      background: #c578dc;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 15px;
    }
    .gallery img {
      width: 100%;
      border-radius: 8px;
    }
    iframe {
      width: 100%;
      height: 300px;
      border: 0;
    }
    footer {
      text-align: center;
      padding: 15px;
      background: #ba4ab2;
      color: #fff;
      margin-top: 40px;
    }
  </style>
</head>
<body><header>
  <h1>Spa Relajarte</h1>
  <p>Tu espacio de descanso y bienestar</p>
</header><!-- LOGIN --><div id="login" class="login-box">
  <h2>Inicio de Sesión</h2>
  <input type="text" id="user" placeholder="Usuario">
  <input type="password" id="pass" placeholder="Contraseña">
  <button onclick="login()">Ingresar</button>
  <p id="loginMsg" style="color:red"></p>
</div><!-- MENU --><nav id="menu" style="display:none">
  <a href="#" onclick="showSection('generales')">Generales</a>
  <a href="#" onclick="showSection('galeria')">Galería</a>
  <a href="#" onclick="showSection('contacto')">Contáctanos</a>
</nav><!-- GENERALES --><section id="generales" class="active">
  <div class="card">
    <h2>Sobre Nuestro Spa</h2>
    <p>
      En <b>Spa Relajarte</b> ofrecemos servicios de masajes terapéuticos, faciales,
      aromaterapia y tratamientos corporales diseñados para reducir el estrés
      y mejorar tu bienestar físico y mental.
    </p>
    <ul>
      <li>Masajes relajantes y descontracturantes</li>
      <li>Tratamientos faciales</li>
      <li>Aromaterapia</li>
      <li>Sauna y spa corporal</li>
    </ul>
  </div>
</section><!-- GALERIA --><section id="galeria">
  <div class="card">
    <h2>Galería</h2>
    <div class="gallery">
      <img src="https://images.unsplash.com/photo-1556228724-4c8b9a1e7f6a" alt="Spa 1">
      <img src="https://images.unsplash.com/photo-1544161515-4ab6ce6db874" alt="Spa 2">
      <img src="https://images.unsplash.com/photo-1519823551278-64ac92734fb1" alt="Spa 3">
      <img src="https://images.unsplash.com/photo-1587019154181-75b3f2c6e37f" alt="Spa 4">
    </div>
  </div>
</section><!-- CONTACTO --><section id="contacto">
  <div class="card">
    <h2>Contáctanos</h2>
    <form>
      <input type="text" placeholder="Nombre">
      <input type="email" placeholder="Correo electrónico">
      <input type="tel" placeholder="Teléfono">
      <textarea rows="4" placeholder="Dudas o comentarios"></textarea>
      <button type="reset">Limpiar</button>
      <button type="submit">Enviar</button>
    </form><h3>Ubicación</h3>
<p>Av #123, Col. Centro, Ciudad de Puebla</p>

<iframe src="https://www.google.com/maps?q=Ciudad%20de%20Puebla&output=embed"></iframe>

  </div>
</section><footer>
  <p>© 2026 Spa Relajarte</p>
</footer><script>
  function login() {
    const user = document.getElementById('user').value;
    const pass = document.getElementById('pass').value;

    if (user === 'admin' && pass === '1234') {
      document.getElementById('login').style.display = 'none';
      document.getElementById('menu').style.display = 'flex';
      showSection('generales');
    } else {
      document.getElementById('loginMsg').innerText = 'Usuario o contraseña incorrectos';
    }
  }

  function showSection(id) {
    const sections = document.querySelectorAll('section');
    sections.forEach(sec => sec.classList.remove('active'));
    document.getElementById(id).classList.add('active');
  }
</script></body>
</html>

