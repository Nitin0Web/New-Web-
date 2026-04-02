<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Maharani Beauty Parlour</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

<style>
body {
  font-family: 'Poppins', sans-serif;
  margin: 0;
  overflow-x: hidden;
  background: linear-gradient(135deg,#ffdde1,#ee9ca7);
}

/* FLOATING BUBBLES FIXED */
.bubbles {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
  pointer-events: none;
}

.bubbles span {
  position: absolute;
  bottom: -100px;
  width: 20px;
  height: 20px;
  background: rgba(255,255,255,0.5);
  border-radius: 50%;
  animation: rise 12s infinite ease-in;
}

.bubbles span:nth-child(1){left:10%; animation-duration:8s;}
.bubbles span:nth-child(2){left:20%; width:30px;height:30px; animation-duration:12s;}
.bubbles span:nth-child(3){left:30%; animation-duration:6s;}
.bubbles span:nth-child(4){left:40%; width:25px;height:25px; animation-duration:10s;}
.bubbles span:nth-child(5){left:50%; animation-duration:7s;}
.bubbles span:nth-child(6){left:60%; width:35px;height:35px; animation-duration:14s;}
.bubbles span:nth-child(7){left:70%; animation-duration:9s;}
.bubbles span:nth-child(8){left:80%; animation-duration:11s;}
.bubbles span:nth-child(9){left:90%; width:28px;height:28px; animation-duration:13s;}
.bubbles span:nth-child(10){left:25%; animation-duration:10s;}

@keyframes rise {
  0% { transform: translateY(0); opacity: 0.7; }
  100% { transform: translateY(-120vh); opacity: 0; }
}

/* CONTENT ABOVE BUBBLES */
header, nav, section, footer {
  position: relative;
  z-index: 1;
}

/* HEADER */
header {
  background: linear-gradient(45deg,#d63384,#ff4d6d);
  color: white;
  padding: 20px;
  text-align: center;
}

/* NAV */
nav {
  background: rgba(255,255,255,0.2);
  backdrop-filter: blur(10px);
  padding: 12px;
  text-align: center;
}

nav a {
  margin: 0 15px;
  color: #d63384;
  text-decoration: none;
  font-weight: bold;
}

/* SECTION */
section {
  padding: 40px 20px;
  text-align: center;
}

/* HERO */
.hero {
  background: linear-gradient(rgba(0,0,0,0.5),rgba(0,0,0,0.5)),
  url('https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9');
  background-size: cover;
  color: white;
  padding: 100px 20px;
}

/* GRID */
.services, .gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(220px,1fr));
  gap: 20px;
}

/* GLASS */
.card, .contact-box {
  background: rgba(255,255,255,0.25);
  backdrop-filter: blur(12px);
  padding: 20px;
  border-radius: 20px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.2);
  transition: 0.3s;
  cursor: pointer;
}

.card:hover {
  transform: translateY(-10px) scale(1.05);
}

.price {
  color:#d63384;
  font-weight:bold;
}

/* BUTTON */
.btn {
  background: linear-gradient(45deg,#d63384,#ff4d6d);
  color:white;
  padding:12px 20px;
  border:none;
  border-radius:25px;
  cursor:pointer;
  transition: 0.3s;
}

.btn:hover {
  transform: scale(1.1);
}

/* GALLERY */
.gallery img {
  width:100%;
  border-radius:15px;
}

/* INPUT */
input, textarea {
  width:90%;
  padding:10px;
  margin:10px 0;
  border-radius:10px;
  border:1px solid #ccc;
}

/* FOOTER */
footer {
  background:#d63384;
  color:white;
  padding:15px;
}
</style>
</head>

<body>

<!-- BUBBLES -->
<div class="bubbles">
  <span></span><span></span><span></span><span></span><span></span>
  <span></span><span></span><span></span><span></span><span></span>
</div>

<header>
<h1>👑 Maharani Beauty Parlour</h1>
<p>Your Beauty, Our Responsibility 💄</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#services">Services</a>
<a href="#gallery">Gallery</a>
<a href="#booking">Booking</a>
<a href="#contact">Contact</a>
</nav>

<section class="hero" id="home">
<h1>Glow Like a Queen ✨</h1>
<p>Best Beauty Services in Your City</p>
<h2 style="background: rgba(0,0,0,0.5); display:inline-block; padding:10px 15px; border-radius:10px;">
🎉 Flat 30% OFF on 1st Visit 🎉
</h2>
<br><br>
<button class="btn" onclick="openWhatsApp('General Inquiry')">Book on WhatsApp</button>
</section>

<section id="services">
<h2>💄 Our Services</h2>
<div class="services">

<div class="card" onclick="openWhatsApp('Facial Service')">
<h3>Facial</h3>
<p class="price">Starting from ₹499</p>
</div>

<div class="card" onclick="openWhatsApp('Hair Styling Service')">
<h3>Hair Styling</h3>
<p class="price">Starting from ₹299</p>
</div>

<div class="card" onclick="openWhatsApp('Bridal Makeup Service')">
<h3>Bridal Makeup</h3>
<p class="price">Starting from ₹4999</p>
</div>

<div class="card" onclick="openWhatsApp('Manicure & Pedicure Service')">
<h3>Manicure & Pedicure</h3>
<p class="price">Starting from ₹399</p>
</div>

<div class="card" onclick="openWhatsApp('Eyebrow Service')">
<h3>Eyebrow</h3>
<p class="price">Starting from ₹39</p>
</div>

</div>
</section>

<section id="gallery">
<h2>📸 Gallery</h2>
<div class="gallery">
<img src="https://images.unsplash.com/photo-1527799820374-dcf8d9d4a388">
<img src="https://images.unsplash.com/photo-1512496015851-a90fb38ba796">
<img src="https://images.unsplash.com/photo-1487412912498-0447578fcca8">
<img src="https://images.unsplash.com/photo-1500840216050-6ffa99d75160">
</div>
</section>

<section id="booking">
<h2>📝 Book Appointment</h2>

<form onsubmit="sendToWhatsApp(); return false;">
<input type="text" id="name" placeholder="Your Name" required><br>
<input type="tel" id="phone" placeholder="Phone Number" required><br>
<textarea id="service" placeholder="Service Required"></textarea><br>
<button class="btn">Submit</button>
</form>

</section>

<section id="contact">
<h2>📞 Contact Us</h2>
<div class="contact-box">
<p><b>Phone:</b> +91 9708401029</p>
<p><b>WhatsApp:</b> +91 7324919240</p>
<p><b>Address:</b> Bus Stand, Rafiganj, Aurangabad, Bihar</p>

<br><br>
<button class="btn" onclick="openWhatsApp('Contact Inquiry')">Chat on WhatsApp</button>
</div>
</section>

<footer>
<p>© 2026 Maharani Beauty Parlour | All Rights Reserved</p>
</footer>

<script>
let whatsappNumber = "917324919240";

/* SERVICE CLICK */
function openWhatsApp(service){
  let message = `Hi 👋 I need enquiry about: ${service}`;
  window.open(`https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`, "_blank");
}

/* FORM SUBMIT */
function sendToWhatsApp(){
  let name = document.getElementById("name").value;
  let phone = document.getElementById("phone").value;
  let service = document.getElementById("service").value;

  let message = `New Appointment Request%0AName: ${name}%0APhone: ${phone}%0AService: ${service}`;

  window.open(`https://wa.me/${whatsappNumber}?text=${message}`, "_blank");
}
</script>

</body>
</html>
