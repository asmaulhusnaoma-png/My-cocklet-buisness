<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ChocoDelight | Premium Chocolate Business</title>

  <style>
    /* Global Styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
      scroll-behavior: smooth;
    }

    body {
      background: linear-gradient(135deg, #3e2723, #5d4037);
      color: #fff;
      overflow-x: hidden;
    }

    /* Header */
    header {
      background: rgba(0, 0, 0, 0.5);
      padding: 20px 10%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 100;
      backdrop-filter: blur(8px);
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
    }

    header h1 {
      font-size: 30px;
      color: #ffcc80;
      letter-spacing: 2px;
      font-weight: 700;
    }

    nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 15px;
      font-weight: 500;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #ffcc80;
    }

    /* 
    Hero Section */
    section.hero {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 0 10%;
      background: url('https://images.unsplash.com') center/cover;
      animation: fadeIn 2s ease;
    }

    section.hero h2 {
      font-size: 3em;
      color: #fff8e1;
      text-shadow: 2px 2px 10px #000;
      animation: fadeInDown 1.5s ease;
    }

    section.hero p {
      margin: 20px 0;
      font-size: 1.2em;
      color: #fbe9e7;
      max-width: 600px;
      animation: fadeInUp 1.5s ease;
    }

    button {
      background: #ffcc80;
      border: none;
      color: #3e2723;
      padding: 12px 25px;
      font-size: 1.1em;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
      animation: fadeIn 2.5s ease;
    }

    button:hover {
      background: #ffe0b2;
      transform: scale(1.05);
    }

    /* 🍫 Product Section */
    section.products {
      padding: 100px 10%;
      background: #4e342e;
      text-align: center;
    }

    section.products h2 {
      font-size: 2.5em;
      color: #ffcc80;
      margin-bottom: 40px;
    }

    .product-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 30px;
    }

    .card {
      background: #5d4037;
      border-radius: 20px;
      overflow: hidden;
      width: 280px;
      transition: 0.3s;
      box-shadow: 0 5px 15px rgba(0,0,0,0.4);
    }

    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 8px 20px rgba(0,0,0,0.6);
    }

    .card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }

    .card h3 {
      color: #ffcc80;
      margin: 15px 0 5px;
    }

    .card p {
      color: #e0cfc7;
      font-size: 0.95em;
      padding: 0 15px 15px;
    }

    /*  About Section */
    section.about {
      padding: 100px 10%;
      background: #3e2723;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 50px;
    }

    .about img {
      width: 400px;
      border-radius: 20px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.5);
    }

    .about-text {
      flex: 1;
      min-width: 300px;
    }

    .about-text h2 {
      color: #ffcc80;
      margin-bottom: 20px;
    }

    .about-text p {
      color: #fbe9e7;
      line-height: 1.6;
      font-size: 1.1em;
    }

    /* Contact Section */
    section.contact {
      background: #4e342e;
      padding: 100px 10%;
      text-align: center;
    }

    section.contact h2 {
      color: #ffcc80;
      margin-bottom: 20px;
      font-size: 2.2em;
    }

    section.contact p {
      color: #e0cfc7;
      margin-bottom: 30px;
    }

    .contact-btn {
      background: #ffcc80;
      color: #3e2723;
      padding: 12px 25px;
      border: none;
      border-radius: 30px;
      font-size: 1.1em;
      cursor: pointer;
      transition: 0.3s;
    }

    .contact-btn:hover {
      background: #ffe0b2;
      transform: scale(1.05);
    }

    /*  Footer */
    footer {
      background: #3e2723;
      text-align: center;
      padding: 25px;
      font-size: 14px;
      color: #d7ccc8;
    }

    /* Animations */
    @keyframes fadeInDown {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    /* 📱 Responsive Design */
    @media (max-width: 768px) {
      header {
        flex-direction: column;
        gap: 10px;
      }

      .about {
        flex-direction: column;
        text-align: center;
      }

      .about img {
        width: 100%;
      }

      .product-container {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
</head>

<body>
  <header>
    <h1>ChocoDelight</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#products">Products</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <h2>Indulge in Pure Chocolate Bliss 🍫</h2>
    <p>Experience premium homemade chocolates crafted with love and perfection. Taste happiness in every bite!</p>
    <button onclick="showMessage()">Order Now</button>
  </section>

  <section class="products" id="products">
    <h2>Our Best chocklets</h2>
    <div class="product-container">
      <div class="card">
        <img src="https://images/Asmaul husna" alt="Dark Chocolate">
        <h3>Dark Delight</h3>
        <p>Rich and bold flavor for true chocolate lovers.</p>
      </div>
      <div class="card">
        <img src="https:" alt="Milk Chocolate">
        <h3>Milky Magic</h3>
        <p>Soft, creamy, and melts in your mouth instantly.</p>
      </div>
      <div class="card">
        <img src="https:" alt="Hazelnut Chocolate">
        <h3>Nutty Heaven</h3>
        <p>Crunchy hazelnuts meet velvety chocolate perfection.</p>
      </div>
    </div>
	
	 <div class="card">
        <img src="https:" alt="Hazelnut Chocolate">
        <h3>Mix fruit chocklets</h3>
        <p>Mixed with many fruits,so a parson can test sweet fruit with chocklets.</p>
      </div>
    </div>
  </section>

  <section class="about" id="about">
    <img src="https://" alt="About ChocoDelight">
    <div class="about-text">0
      <h2>About Us</h2>
      <p>At ChocoDelight, we believe chocolate is more than a treat — it’s an emotion.  
      We source the finest cocoa beans and handcraft every bar with passion and precision.  
      Our mission is to bring happiness to every heart, one bite at a time.</p>
    </div>
  </section>

  <section class="contact" id="contact">
    <h2>Contact Us</h2>
    <p>Have a question or want to place a bulk order? We’d love to hear from you!</p>
    <button class="contact-btn" onclick="contactMessage()">Send Message</button>
  </section>

 
  <script>
    function showMessage() {
      alert(" Thank you for choosing ChocoDelight! Your order journey begins now!");
    }

    function contactMessage() {
      alert("Thanks for reaching out! We'll get back to you soon!");
    }
 
	<footer>
    <p>© 2025 ChocoDelight — Crafted with and Cocoa</p>
  </footer>


  </section>

  <footer>
    <p>© 2025 ChocoDelight — Crafted with and Cocoa</p>
  </footer>

  <script>
    function showMessage() {
      alert("🍫 Thank you for choosing ChocoDelight! Your order journey begins now!");
    }
  </script>
</body>
</html>


</body>
</html>
