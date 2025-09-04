<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aniagu D - Professional Freelance Logo Designer</title>
<meta name="description" content="Aniagu D - Professional freelance logo designer. Minimalist, modern, AI-assisted designs for businesses and personal brands.">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
<style>
/* Reset & Base */
body, html { margin:0; padding:0; font-family:'Poppins',sans-serif; scroll-behavior:smooth; }
a { text-decoration:none; color:inherit; }
img { max-width:100%; display:block; border-radius:10px; }

/* Header */
header {
  background: #1E90FF; color:white; display:flex; justify-content:space-between; align-items:center; padding:15px 30px; position:sticky; top:0; z-index:1000;
}
header nav a { margin-left:20px; font-weight:600; color:white; }
header nav a:hover { text-decoration:underline; }

/* Search Bar */
.search-bar { display:flex; align-items:center; margin-top:10px; }
.search-bar input { padding:6px; border-radius:5px; border:2px solid #1E90FF; flex:1; }
.search-bar button { padding:6px 10px; margin-left:5px; border:none; border-radius:5px; background:#FFA500; color:white; font-weight:bold; cursor:pointer; }
.search-bar button:hover { background:#ffb84d; }

/* Hero */
.hero { text-align:center; background: linear-gradient(135deg,#1E90FF,#FFA500); color:white; padding:80px 20px; }
.hero h1 { font-size:2.8em; margin:20px 0; }
.hero p { font-size:1.2em; margin-bottom:30px; }
.hero a { display:inline-block; margin:10px; padding:12px 25px; border-radius:5px; font-weight:bold; transition:0.3s; }
.hero .hire { background:white; color:#1E90FF; }
.hero .hire:hover { background:#ffd27f; }
.hero .portfolio { background:transparent; border:2px solid white; color:white; }
.hero .portfolio:hover { background:white; color:#1E90FF; }

/* Sections */
section { padding:60px 30px; }
section h2 { color:#1E90FF; margin-bottom:40px; text-align:center; }

/* About */
.about { text-align:center; }
.about img { max-width:150px; border-radius:50%; margin-bottom:20px; }
.about p { line-height:1.6; max-width:800px; margin:0 auto; }

/* Services */
.service-list { display:flex; flex-wrap:wrap; gap:20px; justify-content:center; }
.service-item { background:white; padding:20px; border-radius:10px; width:250px; text-align:center; box-shadow:0 3px 6px rgba(0,0,0,0.1); transition:0.3s; }
.service-item:hover { transform:scale(1.05); box-shadow:0 6px 12px rgba(0,0,0,0.2); }
.service-item h3 { color:#1E90FF; margin-bottom:10px; }

/* Portfolio */
.portfolio-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:20px; }
.portfolio-item { cursor:pointer; overflow:hidden; position:relative; }
.portfolio-item img { transition:transform 0.3s; }
.portfolio-item:hover img { transform:scale(1.05); }

/* Lightbox */
#lightbox { position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.8); display:none; justify-content:center; align-items:center; z-index:2000; }
#lightbox img { max-width:90%; max-height:90%; border-radius:10px; }

/* Testimonials */
.testimonial-carousel { position:relative; max-width:700px; margin:0 auto; overflow:hidden; }
.testimonial-item { text-align:center; font-style:italic; padding:20px; display:none; }
.testimonial-item.active { display:block; }

/* Contact */
.contact-info p { text-align:center; margin:10px 0; }
.contact-form {
  display:flex;
  flex-direction:column;
  gap:10px;
  max-width:500px;
  margin:0 auto;
  text-align:center;
}
.contact-form input, .contact-form textarea, .contact-form button, .contact-form a.button {
  width:100%;
  padding:12px;
  border-radius:5px;
  border:none;
  font-weight:bold;
  text-align:center;
  cursor:pointer;
  transition:0.3s;
}
.contact-form button, .contact-form a.button {
  background: linear-gradient(45deg, #1E90FF, #FFA500);
  color:white;
}
.contact-form button:hover, .contact-form a.button:hover {
  opacity:0.85;
}

/* Footer */
footer { background:#1E90FF; color:white; text-align:center; padding:20px; }

/* Floating Social Buttons */
.floating { position:fixed; bottom:30px; right:30px; display:flex; flex-direction:column; gap:10px; z-index:1000; }
.floating a { background:#1E90FF; color:white; padding:12px; border-radius:50%; display:flex; justify-content:center; align-items:center; font-weight:bold; text-decoration:none; transition:0.3s; }
.floating a:hover { background:#FFA500; }
</style>
</head>
<body>

<!-- Header -->
<header>
<div class="logo"><h1>Aniagu D</h1></div>
<nav>
<a href="#home">Home</a>
<a href="#about">About</a>
<a href="#portfolio">Portfolio</a>
<a href="#services">Services</a>
<a href="#contact">Contact</a>
</nav>
<div class="search-bar">
<input type="text" id="searchInput" placeholder="Search portfolio..." onkeyup="searchPortfolio()">
<button onclick="searchPortfolio()">Search</button>
</div>
</header>

<!-- Hero -->
<section class="hero" id="home">
<h1>Hi! I’m Aniagu D – Freelance Logo Designer</h1>
<p>I create modern, minimalist, and eye-catching logos for businesses and personal brands.</p>
<a href="https://www.fiverr.com/aniagud" class="hire" target="_blank">Hire Me on Fiverr</a>
<a href="#portfolio" class="portfolio">View Portfolio</a>
</section>

<!-- About -->
<section class="about" id="about">
<h2>About Me</h2>
<img src="https://via.placeholder.com/150" alt="Aniagu D">
<p>I’m Aniagu D, a professional freelance designer specializing in Logo Design, Social Media Graphics, and AI-Assisted Illustrations. I help brands look professional and modern.</p>
</section>

<!-- Services -->
<section class="services" id="services">
<h2>My Services</h2>
<div class="service-list">
<div class="service-item"><h3>Logo Design</h3><p>Minimalist, Modern, Mascot logos. AI-assisted logos available.</p></div>
<div class="service-item"><h3>Social Media Graphics</h3><p>Instagram, TikTok, Facebook posts and banners.</p></div>
<div class="service-item"><h3>AI Art / Illustrations</h3><p>Custom AI-generated designs for brands, websites, and social media.</p></div>
<div class="service-item"><h3>Presentation Design</h3><p>Professional slide decks. Editable PowerPoint / Google Slides.</p></div>
</div>
</section>

<!-- Portfolio -->
<section class="portfolio" id="portfolio">
<h2>Portfolio</h2>
<div class="portfolio-grid" id="portfolioGrid">
<div class="portfolio-item"><img src="https://images.unsplash.com/photo-1602524819956-2f5b3ff4f6e6?crop=entropy&cs=tinysrgb&fit=max&h=300&w=400" alt="Minimalist Logo"></div>
<div class="portfolio-item"><img src="https://images.unsplash.com/photo-1593642634367-d91a135587b5?crop=entropy&cs=tinysrgb&fit=max&h=300&w=400" alt="Modern Logo"></div>
<div class="portfolio-item"><img src="https://images.unsplash.com/photo-1612831660866-7d60a1c00c39?crop=entropy&cs=tinysrgb&fit=max&h=300&w=400" alt="Mascot Logo"></div>
<div class="portfolio-item"><img src="https://images.unsplash.com/photo-1593642634302-55b46d918a5f?crop=entropy&cs=tinysrgb&fit=max&h=300&w=400" alt="AI Art"></div>
</div>
</section>

<!-- Lightbox -->
<div id="lightbox" onclick="this.style.display='none';"><img id="lightbox-img"></div>

<!-- Testimonials -->
<section class="testimonials">
<h2>Testimonials</h2>
<div class="testimonial-carousel">
<div class="testimonial-item active">"Excellent work! The logo exceeded my expectations." – Client A</div>
<div class="testimonial-item">"Professional and fast delivery. Highly recommended." – Client B</div>
</div>
</section>

<!-- Contact -->
<section class="contact" id="contact">
<h2>Contact Me</h2>
<div class="contact-info">
<p>📱 WhatsApp: <a href="tel:+2349118790779">09118790779</a></p>
<p>📧 Email: <a href="mailto:aniagudavid7@gmail.com">aniagudavid7@gmail.com</a></p>
<p>💻 Fiverr Profile: <a href="https://www.fiverr.com/aniagud" target="_blank">aniagud</a></p>
</div>

<div class="contact-form">
<form action="YOUR_FORMSPREE_ENDPOINT" method="POST">
<input type="text" name="name" placeholder="Enter your name" required>
<input type="email" name="email" placeholder="Enter your email" required>
<textarea name="message" placeholder="Write your message here" required></textarea>
<button type="submit" class="button">Send Message</button>
</form>
<a href="https://wa.me/2349118790779?text=Hello%20Aniagu%20D!" 
   class="button" target="_blank">Send Message via WhatsApp</a>
<a href="tel:+2349118790779" class="button">Call Me</a>
</div>
</section>

<!-- Footer -->
<footer>
<p>© 202
