<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Monarca Nails Studio</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Georgia, "Times New Roman", serif;
      background: #090909;
      color: #f5f0e8;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: rgba(9, 9, 9, 0.97);
      border-bottom: 1px solid #b8862c;
    }

    .nav-container {
      max-width: 1200px;
      margin: auto;
      padding: 18px 25px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .logo {
      color: #d99022;
      font-size: 25px;
      font-weight: bold;
      letter-spacing: 3px;
      white-space: nowrap;
    }

    .logo span {
      color: #f4c76b;
    }

    .tagline {
      color: #d7c4a2;
      font-size: 11px;
      letter-spacing: 2px;
      margin-top: 2px;
    }

    nav {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
    }

    nav a {
      color: #f2dfbb;
      font-size: 13px;
      transition: 0.3s;
    }

    nav a:hover {
      color: #e89525;
    }

    .hero {
      min-height: 650px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 80px 25px;
      background:
        linear-gradient(rgba(0,0,0,0.65), rgba(0,0,0,0.9)),
        radial-gradient(circle at center, #5c2b08 0%, #181006 35%, #090909 75%);
      border-bottom: 1px solid #5b3a12;
    }

    .hero-content {
      max-width: 850px;
    }

    .butterfly {
      font-size: 75px;
      margin-bottom: 15px;
      filter: drop-shadow(0 0 12px #d99022);
    }

    .hero h1 {
      color: #f0b64c;
      font-size: clamp(38px, 7vw, 76px);
      letter-spacing: 5px;
      text-transform: uppercase;
      line-height: 1.1;
      margin-bottom: 20px;
    }

    .hero h2 {
      color: #f6ead7;
      font-size: clamp(22px, 4vw, 35px);
      font-weight: normal;
      margin-bottom: 20px;
    }

    .hero p {
      color: #d7c4a2;
      font-size: 17px;
      max-width: 650px;
      margin: 0 auto 30px;
    }

    .button {
      display: inline-block;
      background: #d99022;
      color: #120b03;
      padding: 13px 28px;
      border-radius: 3px;
      font-weight: bold;
      letter-spacing: 1px;
      border: 1px solid #f4c76b;
      transition: 0.3s;
      margin: 5px;
    }

    .button:hover {
      background: #f4c76b;
      transform: translateY(-2px);
    }

    .button-outline {
      background: transparent;
      color: #f4c76b;
    }

    .section {
      max-width: 1200px;
      margin: auto;
      padding: 75px 25px;
    }

    .section-title {
      text-align: center;
      margin-bottom: 45px;
    }

    .section-title h2 {
      color: #e5a33a;
      font-size: clamp(28px, 5vw, 42px);
      letter-spacing: 2px;
      margin-bottom: 10px;
    }

    .section-title p {
      color: #bca98b;
      font-size: 15px;
    }

    .gold-line {
      width: 90px;
      height: 2px;
      background: #d99022;
      margin: 15px auto;
    }

    .services-grid,
    .packages-grid,
    .extras-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 22px;
    }

    .card {
      background: #151515;
      border: 1px solid #684719;
      padding: 28px 22px;
      text-align: center;
      border-radius: 5px;
      transition: 0.3s;
    }

    .card:hover {
      border-color: #e5a33a;
      transform: translateY(-5px);
      box-shadow: 0 8px 25px rgba(217, 144, 34, 0.12);
    }

    .card h3 {
      color: #f0b64c;
      font-size: 22px;
      margin-bottom: 12px;
    }

    .card p {
      color: #d2c2a9;
      font-size: 15px;
      margin-bottom: 15px;
    }

    .price {
      color: #e89525;
      font-size: 22px;
      font-weight: bold;
    }

    .package-card {
      background: linear-gradient(145deg, #19130c, #111111);
      border: 1px solid #9b681c;
    }

    .package-card h3 {
      color: #f4c76b;
    }

    .extras-list {
      max-width: 800px;
      margin: auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 12px 30px;
    }

    .extra-item {
      display: flex;
      justify-content: space-between;
      gap: 15px;
      border-bottom: 1px solid #3f2d15;
      padding: 12px 0;
      color: #e1d3bc;
    }

    .extra-item span:last-child {
      color: #e89525;
      font-weight: bold;
      white-space: nowrap;
    }

    .reservation-section {
      background:
        linear-gradient(rgba(20, 12, 4, 0.92), rgba(10, 10, 10, 0.96)),
        radial-gradient(circle at top, #7a3d09, #090909 65%);
      border-top: 1px solid #684719;
      border-bottom: 1px solid #684719;
    }

    .reservation-box {
      max-width: 750px;
      margin: auto;
      background: #121212;
      border: 1px solid #9b681c;
      padding: 35px;
      border-radius: 6px;
    }

    .form-group {
      margin-bottom: 18px;
    }

    .form-group label {
      display: block;
      color: #f0c878;
      margin-bottom: 7px;
      font-size: 14px;
    }

    .form-group input,
    .form-group select,
    .form-group textarea {
      width: 100%;
      padding: 12px;
      background: #090909;
      color: #f5f0e8;
      border: 1px solid #5e431d;
      border-radius: 3px;
      font-family: inherit;
      font-size: 15px;
    }

    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
      outline: none;
      border-color: #e5a33a;
    }

    .form-group textarea {
      min-height: 100px;
      resize: vertical;
    }

    .reservation-info {
      background: #1c1409;
      border-left: 3px solid #d99022;
      padding: 18px;
      margin-bottom: 25px;
      color: #dbc8a8;
      font-size: 14px;
    }

    .reservation-info strong {
      color: #f4c76b;
    }

    .contact-box {
      text-align: center;
      margin-top: 35px;
    }

    .contact-box h3 {
      color: #f0b64c;
      margin-bottom: 10px;
      font-size: 24px;
    }

    .whatsapp {
      display: inline-block;
      margin-top: 12px;
      background: #b8862c;
      color: #0b0b0b;
      padding: 12px 24px;
      border-radius: 4px;
      font-weight: bold;
    }

    .whatsapp:hover {
      background: #f4c76b;
    }

    .policies {
      max-width: 850px;
      margin: auto;
      display: grid;
      gap: 18px;
    }

    .policy {
      background: #151515;
      border-left: 3px solid #d99022;
      padding: 18px 22px;
    }

    .policy h3 {
      color: #f0b64c;
      margin-bottom: 5px;
    }

    .policy p {
      color: #cbb99d;
      font-size: 15px;
    }

    footer {
      text-align: center;
      padding: 35px 20px;
      background: #050505;
      border-top: 1px solid #684719;
      color: #a99577;
      font-size: 14px;
    }

    footer strong {
      color: #e5a33a;
    }

    .success-message {
      display: none;
      margin-top: 20px;
      padding: 18px;
      background: #182514;
      border: 1px solid #668f45;
      color: #d9efc8;
      text-align: center;
    }

    @media (max-width: 850px) {
      .nav-container {
        flex-direction: column;
      }

      nav {
        gap: 10px;
      }

      .hero {
        min-height: 580px;
      }
    }

    @media (max-width: 500px) {
      .logo {
        font-size: 21px;
      }

      .tagline {
        font-size: 9px;
      }

      .reservation-box {
        padding: 22px 17px;
      }

      .section {
        padding: 55px 18px;
      }

      .hero {
        padding: 60px 18px;
      }

      .butterfly {
        font-size: 60px;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="nav-container">
      <div>
        <div class="logo">🦋 MONARCA</div>
        <div class="tagline">NAILS STUDIO · Beauty in every detail ♡</div>
      </div>

      <nav>
        <a href="#inicio">Inicio</a>
        <a href="#servicios">Servicios</a>
        <a href="#paquetes">Paquetes</a>
        <a href="#extras">Extras</a>
        <a href="#reservar">Reservar</a>
        <a href="#politicas">Políticas</a>
      </nav>
    </div>
  </header>

  <section class="hero" id="inicio">
    <div class="hero-content">
      <div class="butterfly">🦋</div>

      <h1>Monarca</h1>

      <h2>Nails Studio</h2>

      <p>
        Donde la belleza de la mariposa Monarca se convierte en arte.
        Realza tu belleza con uñas elegantes, delicadas y llenas de estilo.
      </p>

      <a class="button" href="#reservar">Reservar cita</a>
      <a class="button button-outline" href="#servicios">Ver servicios</a>
    </div>
  </section>

  <section class="section" id="servicios">
    <div class="section-title">
      <h2>Servicios</h2>
      <div class="gold-line"></div>
      <p>Elige el servicio perfecto para ti</p>
    </div>

    <div class="services-grid">
      <div class="card">
        <h3>Soft Gel</h3>
        <p>Uñas elegantes, ligeras y con un acabado natural.</p>
        <div class="price">$50 en adelante</div>
      </div>

      <div class="card">
        <h3>Pintura en Gel</h3>
        <p>Color duradero y brillo hermoso para tus uñas.</p>
        <div class="price">$30</div>
      </div>

      <div class="card">
        <h3>Pintura Regular</h3>
        <p>Un acabado clásico, limpio y bonito.</p>
        <div class="price">$20</div>
      </div>

      <div class="card">
        <h3>Pedicure Regular</h3>
        <p>Cuidado y belleza para tus pies.</p>
        <div class="price">$30</div>
      </div>

      <div class="card">
        <h3>Pedicure Gel</h3>
        <p>Pedicure con color en gel y brillo duradero.</p>
        <div class="price">$40</div>
      </div>
    </div>
  </section>

  <section class="section" id="paquetes">
    <div class="section-title">
      <h2>Paquetes Monarca</h2>
      <div class="gold-line"></div>
      <p>Combina tus servicios y disfruta de nuestros especiales</p>
    </div>

    <div class="packages-grid">
      <div class="card package-card">
        <h3>Monarca Combo</h3>
        <p>Pintura regular + pedicure regular</p>
        <div class="price">$45</div>
      </div>

      <div class="card package-card">
        <h3>Monarca Gel Combo</h3>
        <p>Pintura en gel + pedicure gel</p>
        <div class="price">$65</div>
      </div>

      <div class="card package-card">
        <h3>Monarca Soft Gel Combo</h3>
        <p>Soft gel + pedicure gel</p>
        <div class="price">$85</div>
      </div>

      <div class="card package-card">
        <h3>Combo Mixto</h3>
        <p>Pintura en gel + pedicure regular</p>
        <div class="price">$55</div>
      </div>

      <div class="card package-card">
        <h3>Soft Gel + Regular</h3>
        <p>Soft gel + pedicure regular</p>
        <div class="price">$75</div>
      </div>
    </div>
  </section>

  <section class="section" id="extras">
    <div class="section-title">
      <h2>Extras</h2>
      <div class="gold-line"></div>
      <p>Agrega un detalle especial a tu servicio</p>
    </div>

    <div class="extras-list">
      <div class="extra-item">
        <span>French</span>
        <span>+$5</span>
      </div>

      <div class="extra-item">
        <span>Diseño sencillo</span>
        <span>+$5</span>
      </div>

      <div class="extra-item">
        <span>Diseño elaborado</span>
        <span>+$10</span>
      </div>

      <div class="extra-item">
        <span>Cristales o charms</span>
        <span>+$5</span>
      </div>

      <div class="extra-item">
        <span>Reparación</span>
        <span>+$5</span>
      </div>

      <div class="extra-item">
        <span>Retiro Soft Gel</span>
        <span>+$10</span>
      </div>

      <div class="extra-item">
        <span>Retiro Gel</span>
        <span>+$5</span>
      </div>
    </div>
  </section>

  <section class="reservation-section" id="reservar">
    <div class="section">
      <div class="section-title">
        <h2>Reserva tu cita</h2>
        <div class="gold-line"></div>
        <p>Completa el formulario para solicitar tu reserva</p>
      </div>

      <div class="reservation-box">
        <div class="reservation-info">
          <strong>Importante:</strong>
          Para confirmar tu cita se requiere un depósito de
          <strong>$20</strong>. El depósito puede realizarse en efectivo o por Zelle.
          Después de enviar tu solicitud, nos comunicaremos contigo para confirmar
          la disponibilidad y los detalles del pago.
        </div>

        <form id="reservationForm">
          <div class="form-group">
            <label for="name">Nombre completo</label>
            <input type="text" id="name" required>
          </div>

          <div class="form-group">
            <label for="service">Servicio</label>
            <select id="service" required>
              <option value="">Selecciona un servicio</option>
              <option>Soft Gel - $50 en adelante</option>
              <option>Pintura en Gel - $30</option>
              <option>Pintura Regular - $20</option>
              <option>Pedicure Regular - $30</option>
              <option>Pedicure Gel - $40</option>
              <option>Monarca Combo - $45</option>
              <option>Monarca Gel Combo - $65</option>
              <option>Monarca Soft Gel Combo - $85</option>
              <option>Combo Mixto - $55</option>
              <option>Soft Gel + Regular - $75</option>
            </select>
          </div>

          <div class="form-group">
            <label for="date">Fecha preferida</label>
            <input type="date" id="date" required>
          </div>

          <div class="form-group">
            <label for="time">Hora preferida</label>
            <input type="time" id="time" required>
          </div>

          <div class="form-group">
            <label for="phone">Teléfono</label>
            <input type="tel" id="phone" required>
          </div>

          <div class="form-group">
            <label for="details">Detalles o extras</label>
            <textarea id="details" placeholder="Escribe aquí si deseas French, diseños, cristales u otro detalle."></textarea>
          </div>

          <button class="button" type="submit">
            Enviar solicitud de reserva
          </button>

          <div class="success-message" id="successMessage">
            Tu solicitud está lista. Ahora serás dirigida a WhatsApp para enviarla.
          </div>
        </form>
      </div>

      <div class="contact-box">
        <h3>¿Tienes alguna pregunta?</h3>
        <p>Escríbenos directamente por WhatsApp para más información.</p>

        <a
          class="whatsapp"
          href="https://wa.me/17868588959"
          target="_blank"
        >
          💬 Escribir por WhatsApp
        </a>
      </div>
    </div>
  </section>

  <section class="section" id="politicas">
    <div class="section-title">
      <h2>Políticas</h2>
      <div class="gold-line"></div>
      <p>Información importante antes de reservar</p>
    </div>

    <div class="policies">
      <div class="policy">
        <h3>Depósito</h3>
        <p>
          Se requiere un depósito de $20 para confirmar la cita.
          El depósito se descuenta del total del servicio.
        </p>
      </div>

      <div class="policy">
        <h3>Cancelaciones</h3>
        <p>
          Para cancelar o cambiar una cita, avisa con al menos 24 horas
          de anticipación. Los depósitos pueden no ser reembolsables
          en cancelaciones tardías o ausencias.
        </p>
      </div>

      <div class="policy">
        <h3>Tolerancia</h3>
        <p>
          Se permite una tolerancia de 10 minutos. Después de ese tiempo,
          la cita puede considerarse cancelada o requerir un cambio de horario.
        </p>
      </div>

      <div class="policy">
        <h3>Confirmación</h3>
        <p>
          La cita no queda confirmada hasta recibir la confirmación
          por WhatsApp y completar el depósito requerido.
        </p>
      </div>
    </div>
  </section>

  <footer>
    <p>
      © 2026 <strong>Monarca Nails Studio</strong>.
      Todos los derechos reservados.
    </p>
    <p>Beauty in every detail ♡</p>
  </footer>

  <script>
    document
      .getElementById("reservationForm")
      .addEventListener("submit", function(event) {
        event.preventDefault();

        const name = document.getElementById("name").value;
        const service = document.getElementById("service").value;
        const date = document.getElementById("date").value;
        const time = document.getElementById("time").value;
        const phone = document.getElementById("phone").value;
        const details = document.getElementById("details").value;

        const message =
          "Hola, quiero solicitar una reserva en Monarca Nails Studio.%0A%0A" +
          "Nombre: " + encodeURIComponent(name) + "%0A" +
          "Servicio: " + encodeURIComponent(service) + "%0A" +
          "Fecha: " + encodeURIComponent(date) + "%0A" +
          "Hora: " + encodeURIComponent(time) + "%0A" +
          "Teléfono: " + encodeURIComponent(phone) + "%0A" +
          "Detalles: " + encodeURIComponent(details) + "%0A%0A" +
          "Entiendo que se requiere un depósito de $20 para confirmar la cita.";

        document.getElementById("successMessage").style.display = "block";

        setTimeout(function() {
          window.open(
            "https://wa.me/17868588959?text=" + message,
            "_blank"
          );
        }, 800);
      });
  </script>

</body>
</html>
