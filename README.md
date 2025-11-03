<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Control del Sur - Manejo Integral de Plagas</title>
  <style>
    body {
      margin: 0;
      font-family: "Segoe UI", Arial, sans-serif;
      background-color: #e5ebe2;
      color: #333;
      scroll-behavior: smooth;
    }

    header {
      background-color: #a4b3a1;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px 40px;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }

    header img {
      height: 60px;
    }

    nav {
      display: flex;
      align-items: center;
    }

    nav a {
      color: #2e2e2e;
      text-decoration: none;
      margin: 0 15px;
      font-weight: bold;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #000;
    }

    .menu-toggle {
      display: none;
      flex-direction: column;
      cursor: pointer;
    }

    .menu-toggle span {
      height: 3px;
      width: 25px;
      background: #2e2e2e;
      margin: 4px 0;
      border-radius: 5px;
      transition: 0.4s;
    }

    @media (max-width: 768px) {
      nav {
        display: none;
        flex-direction: column;
        background-color: #a4b3a1;
        position: absolute;
        top: 80px;
        right: 0;
        width: 100%;
        text-align: center;
      }

      nav.show {
        display: flex;
      }

      .menu-toggle {
        display: flex;
      }
    }

    .hero {
      background: url("https://controldelsur.com.ar/images/fumigacion-hogar.jpg") center/cover no-repeat;
      color: white;
      text-align: center;
      padding: 120px 20px;
      position: relative;
    }

    .hero::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background-color: rgba(0,0,0,0.5);
    }

    .hero h1, .hero p {
      position: relative;
      z-index: 1;
    }

    .hero h1 {
      font-size: 2.8em;
      margin-bottom: 10px;
    }

    section {
      padding: 60px 20px;
      text-align: center;
    }

    h2 {
      font-size: 2em;
      color: #2f4033;
    }

    .servicios {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }

    .servicio {
      background: #f7f7f7;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .servicio:hover {
      transform: translateY(-5px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.3);
    }

    .servicio img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }

    .servicio h3 {
      margin: 15px 0 10px;
      color: #344437;
    }

    .servicio p {
      padding: 0 15px 20px;
      color: #555;
    }

    form {
      max-width: 600px;
      margin: 30px auto;
      background: #f7f7f7;
      padding: 25px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }

    form input, form textarea {
      width: 100%;
      padding: 12px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 1em;
      font-family: inherit;
      resize: none;
    }

    form button {
      background-color: #344437;
      color: white;
      border: none;
      padding: 12px 20px;
      border-radius: 6px;
      cursor: pointer;
      font-size: 1em;
      transition: background 0.3s;
    }

    form button:hover {
      background-color: #2a352b;
    }

    footer {
      background-color: #a4b3a1;
      color: #2e2e2e;
      text-align: center;
      padding: 20px;
      font-size: 0.9em;
    }

    .fade-in {
      opacity: 0;
      transform: translateY(40px);
      transition: all 1s ease-out;
    }

    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .whatsapp-float {
      position: fixed;
      width: 60px;
      height: 60px;
      bottom: 20px;
      right: 20px;
      background-color: #25D366;
      color: white;
      border-radius: 50%;
      text-align: center;
      font-size: 30px;
      box-shadow: 2px 2px 10px rgba(0,0,0,0.3);
      z-index: 1000;
      transition: transform 0.3s;
    }

    .whatsapp-float:hover {
      transform: scale(1.1);
    }

    .whatsapp-float img {
      width: 35px;
      margin-top: 12px;
    }
  </style>
</head>
<body>

  <header>
    <img src="https://controldelsur.com.ar/images/logo_head2.png" alt="Control del Sur Logo">
    <div class="menu-toggle" id="menu-toggle">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <nav id="navbar">
      <a href="#inicio">Inicio</a>
      <a href="#servicios">Servicios</a>
      <a href="#nosotros">Nosotros</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </header>

  <section id="inicio" class="hero">
    <h1>Control del Sur</h1>
    <p>Expertos en Manejo Integral de Plagas Urbanas y Agrícolas</p>
  </section>

  <section id="servicios">
    <h2>Nuestros Servicios</h2>
    <div class="servicios">
      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/fumigacion-hogar.jpg" alt="Fumigación en Hogar">
        <h3>Fumigación Hogar</h3>
        <p>Tratamientos domiciliarios seguros y efectivos contra insectos y roedores.</p>
      </div>

      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/fumigacion-oficinas.jpg" alt="Fumigación en Oficinas">
        <h3>Fumigación Oficinas</h3>
        <p>Control preventivo y correctivo para ambientes de trabajo y espacios comunes.</p>
      </div>

      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/fumigacion-silos.jpg" alt="Fumigación de Silos">
        <h3>Fumigación Silos</h3>
        <p>Servicios especializados para silos y almacenamiento a granel.</p>
      </div>

      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/fumigacion-granos.jpg" alt="Fumigación de Granos">
        <h3>Fumigación de Granos</h3>
        <p>Protección y preservación de granos durante almacenamiento y transporte.</p>
      </div>

      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/fumigacion-contenedor2.jpg" alt="Fumigación de Contenedores">
        <h3>Fumigación Contenedores I</h3>
        <p>Tratamientos para contenedores y carga para evitar plagas en import/export.</p>
      </div>

      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/fumigacion-contenedor.jpg" alt="Fumigación de Contenedores">
        <h3>Fumigación Contenedores II</h3>
        <p>Soluciones para diferentes tipos de contenedores y cargas sensibles.</p>
      </div>

      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/acondicionamiento-contenedor1.jpg" alt="Acondicionamiento de Contenedores">
        <h3>Acondicionamiento de Contenedores</h3>
        <p>Preparación y acondicionamiento para almacenamiento seguro de mercancías.</p>
      </div>

      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/muestras-celerales.jpg" alt="Muestras y Análisis Cereal">
        <h3>Muestras y Análisis</h3>
        <p>Toma de muestras y análisis de calidad para granos y productos almacenados.</p>
      </div>

      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/contenedor-liner.jpg" alt="Liner para Contenedores">
        <h3>Liners para Contenedores</h3>
        <p>Instalación de liners y protección interna para transporte de granos.</p>
      </div>

      <div class="servicio">
        <img src="https://controldelsur.com.ar/images/contenedor-cargado.jpg" alt="Contenedor Cargado">
        <h3>Inspección de Cargas</h3>
        <p>Inspección y control de cargas antes del embarque y recepción.</p>
      </div>
    </div>
  </section>

  <section id="nosotros">
    <h2>Sobre Nosotros</h2>
    <p>En <strong>Control del Sur</strong> contamos con un equipo profesional especializado en el manejo integral de plagas urbanas y agrícolas. Ofrecemos soluciones seguras, certificadas y personalizadas para cada cliente, priorizando la salud, la higiene y la sostenibilidad ambiental.</p>
  </section>

  <section id="contacto">
    <h2>Contacto</h2>
    <form id="contactForm">
      <input type="text" id="nombre" placeholder="Tu nombre" required>
      <input type="email" id="email" placeholder="Tu correo electrónico" required>
      <textarea id="mensaje" rows="5" placeholder="Escribí tu mensaje..." required></textarea>
      <button type="submit">Enviar por WhatsApp</button>
    </form>
  </section>

  <a href="https://wa.me/5492910000000" target="_blank" class="whatsapp-float">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp">
  </a>

  <footer>
    © 2025 Control del Sur - Todos los derechos reservados.
  </footer>

  <script>
    const elements = document.querySelectorAll('.fade-in');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) entry.target.classList.add('visible');
      });
    }, { threshold: 0.3 });

    elements.forEach(el => observer.observe(el));

    const form = document.getElementById('contactForm');
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const nombre = document.getElementById('nombre').value;
      const email = document.getElementById('email').value;
      const mensaje = document.getElementById('mensaje').value;
      const numero = "5492910000000";
      const url = `https://wa.me/${numero}?text=👋 Hola, soy ${nombre}.%0A📧 Email: ${email}%0A💬 Mensaje: ${mensaje}`;
      window.open(url, "_blank");
    });

    // Menú hamburguesa
    const menuToggle = document.getElementById('menu-toggle');
    const navbar = document.getElementById('navbar');
    menuToggle.addEventListener('click', () => {
      navbar.classList.toggle('show');
    });
  </script>

</body>
</html>

