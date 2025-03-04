<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dialysis Consulting Center (DCC)</title>
  <!-- Google Fonts -->
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Lora:wght@400;700&display=swap"
    rel="stylesheet"
  />
  <style>
    /* =============== Global Reset & Base Styles =============== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    html, body {
      width: 100%;
      height: 100%;
      font-family: 'Inter', sans-serif;
      color: #333;
      background-color: #f5f5f5;
      scroll-behavior: smooth;
    }
    img {
      max-width: 100%;
      display: block;
    }
    a {
      text-decoration: none;
      color: inherit;
    }
    .container {
      width: 90%;
      max-width: 1200px;
      margin: auto;
      padding: 0 20px;
    }

    /* =============== Navbar =============== */
    header {
      position: sticky;
      top: 0;
      width: 100%;
      background-color: #fff;
      box-shadow: 0 1px 4px rgba(0, 0, 0, 0.1);
      z-index: 999;
    }
    .navbar-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 1rem 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .navbar-brand {
      font-weight: 700;
      font-size: 1.25rem;
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 2rem;
    }
    nav li {
      font-weight: 600;
    }
    nav a:hover {
      color: #666;
    }

    /* =============== Hero Section =============== */
    .hero {
      background: 
        linear-gradient(rgba(0, 0, 0, 0.45), rgba(0, 0, 0, 0.45)), 
        url('https://via.placeholder.com/1600x900') center center/cover no-repeat;
      height: 80vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: #fff;
    }
    .hero-content {
      max-width: 800px;
      padding: 0 1rem;
    }
    .hero h1 {
      font-size: 3rem;
      font-weight: 700;
      margin-bottom: 1rem;
    }
    .hero p {
      font-size: 1.3rem;
      margin-bottom: 2rem;
      line-height: 1.6;
    }
    .cta-btn {
      display: inline-block;
      padding: 0.75rem 1.5rem;
      background-color: #000;
      color: #fff;
      border-radius: 5px;
      font-weight: 600;
      transition: background-color 0.3s ease;
    }
    .cta-btn:hover {
      background-color: #333;
    }

    /* =============== About, Mission & Messaging Section =============== */
    .about {
      max-width: 1200px;
      margin: 3rem auto;
      padding: 0 2rem;
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      align-items: center;
    }
    .about img {
      flex: 1 1 400px;
      border-radius: 8px;
    }
    .about-text {
      flex: 1 1 400px;
    }
    .about-text h2 {
      font-size: 2rem;
      font-weight: 700;
      margin-bottom: 1rem;
    }
    .about-text p {
      color: #555;
      line-height: 1.6;
      margin-bottom: 1.5rem;
      font-size: 1.1rem;
    }
    .mission {
      background-color: #fff;
      padding: 40px 20px;
      border-left: 6px solid #ff6600;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      border-radius: 8px;
      margin-bottom: 2rem;
    }
    .mission h3 {
      font-family: 'Lora', serif;
      font-size: 1.5rem;
      margin-bottom: 10px;
    }
    .mission p {
      font-size: 1rem;
      color: #555;
      line-height: 1.6;
    }

    /* =============== Services Section =============== */
    .services {
      max-width: 1200px;
      margin: 3rem auto;
      padding: 0 2rem;
      text-align: center;
    }
    .services h2 {
      font-size: 2.5rem;
      margin-bottom: 20px;
      font-weight: 700;
    }
    .services p {
      max-width: 800px;
      margin: 0 auto 20px;
      color: #555;
      line-height: 1.6;
      font-size: 1.1rem;
    }
    .service-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      margin-top: 2rem;
    }
    .service-item {
      background-color: #fff;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.08);
      transition: transform 0.3s ease;
    }
    .service-item:hover {
      transform: translateY(-5px);
    }
    .service-item h3 {
      margin-bottom: 1rem;
      font-weight: 700;
      font-size: 1.25rem;
    }
    .service-item p {
      color: #666;
      line-height: 1.5;
      font-size: 0.95rem;
    }

    /* =============== Case Studies Section =============== */
    .case-studies {
      max-width: 1200px;
      margin: 3rem auto;
      padding: 0 2rem;
      text-align: center;
    }
    .case-studies h2 {
      font-size: 2.5rem;
      margin-bottom: 20px;
      font-weight: 700;
      color: var(--primary);
    }
    .case-studies p {
      max-width: 800px;
      margin: 0 auto 2rem;
      color: #555;
      line-height: 1.6;
      font-size: 1.1rem;
    }
    .case-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }
    .case-item {
      background: #fff;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.08);
      text-align: left;
    }
    .case-item h3 {
      font-family: 'Lora', serif;
      margin-bottom: 10px;
      font-size: 1.5rem;
      color: var(--primary);
    }
    .case-item p {
      font-size: 1rem;
      color: #666;
      line-height: 1.5;
    }

    /* =============== Contact Section =============== */
    .contact {
      max-width: 1200px;
      margin: 3rem auto;
      padding: 0 2rem;
    }
    .contact h2 {
      text-align: center;
      font-size: 2rem;
      font-weight: 700;
      margin-bottom: 1rem;
    }
    .contact p {
      text-align: center;
      max-width: 700px;
      margin: 0.5rem auto 2rem;
      color: #555;
      line-height: 1.6;
      font-size: 1.1rem;
    }
    .contact-details {
      text-align: center;
      margin-bottom: 2rem;
      font-size: 1rem;
      color: #333;
      font-weight: 600;
    }
    .contact-form {
      max-width: 600px;
      margin: 0 auto;
      background-color: #fff;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.08);
    }
    .contact-form label {
      display: block;
      margin-bottom: 0.5rem;
      font-weight: 600;
    }
    .contact-form input,
    .contact-form textarea {
      width: 100%;
      padding: 0.75rem;
      margin-bottom: 1rem;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 1rem;
    }
    .contact-form button {
      display: inline-block;
      padding: 0.75rem 1.5rem;
      background-color: #000;
      color: #fff;
      border-radius: 5px;
      font-weight: 600;
      transition: background-color 0.3s ease;
      cursor: pointer;
      border: none;
    }
    .contact-form button:hover {
      background-color: #333;
    }

    /* =============== Footer =============== */
    footer {
      background-color: #fff;
      box-shadow: 0 -1px 4px rgba(0, 0, 0, 0.1);
      padding: 1.5rem 2rem;
      text-align: center;
      margin-top: 3rem;
    }
    footer p {
      font-size: 0.9rem;
      color: #666;
    }
    .footer-links {
      margin-top: 1rem;
    }
    .footer-links a {
      margin: 0 0.5rem;
      font-weight: 600;
      color: #333;
    }
    .footer-links a:hover {
      color: #666;
    }

    /* =============== Responsive Design =============== */
    @media (max-width: 768px) {
      .about {
        flex-direction: column;
      }
      .about img,
      .about-text {
        flex: 1 1 auto;
      }
      .navbar-container {
        flex-direction: column;
      }
      nav ul {
        margin-top: 1rem;
      }
    }
  </style>
</head>
<body>
  <!-- Navbar -->
  <header>
    <div class="navbar-container container">
      <div class="navbar-brand">DCC</div>
      <nav>
        <ul>
          <li><a href="#hero">Home</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#case-studies">Case Studies</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero" id="hero">
    <div class="hero-content container">
      <h1>Build Something Amazing</h1>
      <p>
        Welcome to Dialysis Consulting Center (DCC). We empower dialysis centers to grow and extend essential care to underserved communities.
      </p>
      <a href="#contact" class="cta-btn">Work With Us</a>
    </div>
  </section>

  <!-- Services Section -->
  <section class="services" id="services">
    <div class="container">
      <h2>Our Services</h2>
      <p>
        We offer strategic consulting to help dialysis centers expand, optimize operations, and deliver sustainable growth—while also supporting organizations dedicated to increasing access to dialysis treatment.
      </p>
      <div class="service-grid">
        <div class="service-item">
          <h3>Growth & Expansion Strategy</h3>
          <p>
            Tailored plans to expand your dialysis services into new locations and communities.
          </p>
        </div>
        <div class="service-item">
          <h3>Operational Efficiency</h3>
          <p>
            Data-driven insights to optimize operations and improve patient care.
          </p>
        </div>
        <div class="service-item">
          <h3>Regulatory & Compliance Guidance</h3>
          <p>
            Expert support to navigate healthcare regulations and ensure compliance.
          </p>
        </div>
        <div class="service-item">
          <h3>Financial & Risk Management</h3>
          <p>
            Strategic planning and risk management solutions to secure your future.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- About & Mission Section -->
  <section class="about" id="about">
    <img src="https://via.placeholder.com/500x400" alt="About DCC" />
    <div class="about-text">
      <h2>About DCC</h2>
      <div class="mission">
        <h3>Our Mission</h3>
        <p>
          At Dialysis Consulting Center (DCC), our mission is to empower dialysis centers to thrive while expanding critical treatment services to communities in need. We partner with organizations committed to increasing healthcare access, delivering innovative solutions that drive sustainable growth and improved patient outcomes.
        </p>
      </div>
      <p>
        With deep industry expertise and a proven track record, DCC offers comprehensive strategic consulting—from growth planning and operational efficiency to regulatory compliance and financial management—to help you succeed in a rapidly evolving healthcare landscape.
      </p>
    </div>
  </section>

  <!-- Case Studies Section -->
  <section class="case-studies" id="case-studies">
    <div class="container">
      <h2>Case Studies</h2>
      <p>
        Discover how we've helped dialysis centers and healthcare organizations achieve measurable success.
      </p>
      <div class="case-grid">
        <div class="case-item">
          <h3>Expansion Success Story</h3>
          <p>
            We developed a tailored expansion strategy for a regional dialysis center, resulting in a 35% increase in service capacity and improved patient outcomes.
          </p>
        </div>
        <div class="case-item">
          <h3>Operational Transformation</h3>
          <p>
            Through data-driven analysis, we optimized workflows and reduced operational costs by 20% for a healthcare provider, enabling reinvestment into patient care.
          </p>
        </div>
        <div class="case-item">
          <h3>Compliance & Financial Restructuring</h3>
          <p>
            Our regulatory and financial advisory helped a dialysis center secure new funding and achieve full compliance with industry standards.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="contact" id="contact">
    <div class="container">
      <h2>Get in Touch</h2>
      <p>
        Ready to transform your organization and expand your impact? Reach out today to learn how DCC can help you grow.
      </p>
      <div class="contact-details">
        4400 NE 77TH Ave Suite 275<br />
        Vancouver, WA 98662
      </div>
      <div class="contact-form">
        <form action="mailto:your-email@example.com" method="post" enctype="text/plain">
          <label for="name">Name</label>
          <input type="text" id="name" name="name" placeholder="Your Name" required />

          <label for="email">Email</label>
          <input type="email" id="email" name="email" placeholder="Your Email" required />

          <label for="message">Message</label>
          <textarea
            id="message"
            name="message"
            rows="5"
            placeholder="How can we help you?"
            required
          ></textarea>

          <button type="submit">Send Message</button>
        </form>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <p>&copy; 2025 Dialysis Consulting Center (DCC). All rights reserved.</p>
      <div class="footer-links">
        <a href="https://www.linkedin.com" target="_blank">LinkedIn</a>|
        <a href="https://twitter.com" target="_blank">Twitter</a>|
        <a href="https://github.com" target="_blank">GitHub</a>
      </div>
    </div>
  </footer>
</body>
</html>
