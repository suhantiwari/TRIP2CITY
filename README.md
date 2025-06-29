# TRIP2CITY
welcome to patna to samstipur your one stop destination for unforgettable journeys
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Patna to Samastipur Travels</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet" />
<style>
  /* Reset & basics */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: #eee;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
  a {
    color: #00fff7;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  a:hover {
    color: #ff00ea;
  }

  /* Container for sections */
  .container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto 60px;
  }

  /* Hero Section */
  header {
    position: relative;
    height: 70vh;
    background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1470&q=80') center/cover no-repeat;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #00fff7;
    text-shadow:
      0 0 5px #00fff7,
      0 0 10px #00fff7,
      0 0 20px #00fff7;
    font-size: 2.5rem;
    font-weight: 600;
    flex-direction: column;
    text-align: center;
  }
  header::after {
    content: "";
    position: absolute;
    inset: 0;
    background: rgba(0, 0, 0, 0.6);
  }
  header > * {
    position: relative;
    z-index: 1;
  }
  header button {
    margin-top: 20px;
    background: transparent;
    border: 2px solid #00fff7;
    color: #00fff7;
    padding: 12px 30px;
    border-radius: 30px;
    cursor: pointer;
    font-size: 1.1rem;
    transition: 0.4s ease;
    box-shadow:
      0 0 5px #00fff7,
      0 0 10px #00fff7,
      0 0 20px #00fff7;
  }
  header button:hover {
    background: #00fff7;
    color: #0b1a1f;
    box-shadow:
      0 0 15px #00fff7,
      0 0 30px #00fff7;
  }

  /* Section Titles */
  h2.section-title {
    text-align: center;
    margin-bottom: 40px;
    font-size: 2.2rem;
    color: #ff00ea;
    text-shadow:
      0 0 5px #ff00ea,
      0 0 10px #ff00ea;
  }

  /* About Us */
  #about {
    background: rgba(255 0 234 / 0.05);
    padding: 40px 20px;
    border-radius: 15px;
    box-shadow:
      0 0 15px rgba(255, 0, 234, 0.3);
  }
  #about p {
    font-size: 1.1rem;
    line-height: 1.6;
    max-width: 900px;
    margin: 0 auto;
    color: #ddd;
  }

  /* Cards Grid */
  .cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 25px;
  }

  /* Car & Packages Cards */
  .card {
    background: #111;
    border-radius: 15px;
    box-shadow:
      0 0 10px #00fff7,
      inset 0 0 10px #0ff;
    color: #eee;
    width: 280px;
    display: flex;
    flex-direction: column;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .card:hover {
    transform: translateY(-10px);
    box-shadow:
      0 0 20px #ff00ea,
      inset 0 0 20px #ff00ea;
  }
  .card img {
    width: 100%;
    height: 160px;
    object-fit: cover;
  }
  .card-content {
    padding: 20px;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .card-content h3 {
    margin-bottom: 12px;
    color: #00fff7;
    text-shadow:
      0 0 5px #00fff7;
  }
  .card-content p {
    flex-grow: 1;
    font-size: 0.95rem;
    line-height: 1.4;
    color: #ccc;
  }
  .price {
    font-weight: 700;
    font-size: 1.2rem;
    margin: 15px 0;
    color: #ff00ea;
    text-shadow:
      0 0 7px #ff00ea;
  }
  .card button {
    background: transparent;
    border: 2px solid #ff00ea;
    color: #ff00ea;
    padding: 10px 20px;
    border-radius: 30px;
    cursor: pointer;
    font-weight: 600;
    transition: all 0.3s ease;
    align-self: center;
    box-shadow:
      0 0 8px #ff00ea;
  }
  .card button:hover {
    background: #ff00ea;
    color: #111;
    box-shadow:
      0 0 20px #ff00ea,
      0 0 30px #ff00ea;
  }

  /* Contact Section */
  #contact {
    background: rgba(0, 255, 247, 0.05);
    padding: 40px 20px;
    border-radius: 15px;
    box-shadow:
      0 0 15px rgba(0, 255, 247, 0.3);
    text-align: center;
  }
  #contact p {
    font-size: 1.2rem;
    color: #00fff7;
    text-shadow:
      0 0 7px #00fff7;
    margin-bottom: 15px;
  }
  #contact a.phone {
    font-size: 1.5rem;
    font-weight: 700;
    color: #ff00ea;
    text-shadow:
      0 0 10px #ff00ea;
  }
  #contact a.phone:hover {
    color: #00fff7;
    text-shadow:
      0 0 15px #00fff7;
  }

  /* Footer */
  footer {
    background: #111;
    color: #555;
    text-align: center;
    padding: 15px 10px;
    box-shadow:
      0 -2px 10px #ff00ea inset;
  }
  footer nav a {
    margin: 0 15px;
    font-weight: 600;
    color: #666;
    text-shadow: none;
  }
  footer nav a:hover {
    color: #ff00ea;
    text-shadow:
      0 0 8px #ff00ea;
  }

  /* Responsive */
  @media (max-width: 900px) {
    .cards {
      justify-content: center;
    }
  }
  @media (max-width: 700px) {
    header {
      font-size: 1.8rem;
      height: 50vh;
      padding: 0 10px;
    }
    .card {
      width: 100%;
      max-width: 350px;
    }
  }
</style>
</head>
<body>

<header>
  <h1>Patna to Samastipur Travels</h1>
  <p>Your trusted partner for unforgettable journeys in Bihar</p>
  <button>Book Now</button>
</header>

<main class="container">

  <section id="about">
    <h2 class="section-title">About Us</h2>
    <p>
      Welcome to Patna to Samastipur Travels — your go-to travel agency for safe, comfortable, and affordable trips across Bihar. With years of experience, we provide excellent cab services, group tours, and customized travel packages designed to meet your needs. Join thousands of happy travelers exploring the beauty of Bihar with us!
    </p>
  </section>

  <section id="cars" style="margin-top:60px;">
    <h2 class="section-title">Choose Your Ride</h2>
    <div class="cards">

      <article class="card">
        <img src="https://cdn.pixabay.com/photo/2014/04/03/10/32/sedan-309489_1280.png" alt="Sedan Car" />
        <div class="card-content">
          <h3>Sedan Car</h3>
          <p>Comfortable and fuel-efficient sedan perfect for small groups and city rides.</p>
          <div class="price">₹3000 / day</div>
          <button>Book Now</button>
        </div>
      </article>

      <article class="card">
        <img src="https://cdn.pixabay.com/photo/2016/11/29/03/53/suv-1869510_1280.png" alt="SUV Car" />
        <div class="card-content">
          <h3>SUV Car</h3>
          <p>Spacious and powerful SUV ideal for family trips and rough terrains.</p>
          <div class="price">₹5000 / day</div>
          <button>Book Now</button>
        </div>
      </article>

    </div>
  </section>

  <section id="packages" style="margin-top:60px;">
    <h2 class="section-title">Travel Packages</h2>
    <div class="cards">

      <article class="card">
        <img src="https://images.unsplash.com/photo-1501594907352-04cda38ebc29?auto=format&fit=crop&w=800&q=80" alt="Patna to Samastipur" />
        <div class="card-content">
          <h3>Patna to Samastipur Round Trip</h3>
          <p>Explore the scenic route between Patna and Samastipur with our affordable round-trip package. Includes cab and guide.</p>
          <div class="price">₹4500</div>
          <button>Book Now</button>
        </div>
      </article>

      <article class="card">
        <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=800&q=80" alt="Group Tour" />
        <div class="card-content">
          <h3>Group Tour Package</h3>
          <p>Perfect for friends and family! Includes transport, hotel stay, and sightseeing across Bihar.</p>
          <div class="price">₹15000 (for 5 people)</div>
          <button>Book Now</button>
        </div>
      </article>

      <article class="card">
        <img src="https://images.unsplash.com/photo-1468071174046-657d9d351a40?auto=format&fit=crop&w=800&q=80" alt="Custom Tours" />
        <div class="card-content">
          <h3>Customizable Tour Plans</h3>
          <p>Create your own travel itinerary with personalized cab services and package options tailored to your preferences.</p>
          <div class="price">Starting ₹7000</div>
          <button>Book Now</button>
        </div>
      </article>

    </div>
  </section>

  <section id="contact" style="margin-top:60px;">
    <h2 class="section-title">Contact Us</h2>
    <p>Have questions? Want to book your trip now?</p>
    <a href="tel:+919211241677" class="phone">📞 9211241677</a>
  </section>

</main>

<footer>
  <nav>
    <a href="#about">About</a> |
    <a href="#cars">Cars</a> |
    <a href="#packages">Packages</a> |
    <a href="#contact">Contact</a>
  </nav>
  <p>© 2025 Patna to Samastipur Travels. All rights reserved.</p>
</footer>

</body>
</html>
