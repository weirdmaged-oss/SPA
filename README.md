
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
<p>Av. Bienestar #123, Col. Centro, Ciudad de México</p>

<iframe src="https://www.google.com/maps?q=Ciudad%20de%20Mexico&output=embed"></iframe>

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


