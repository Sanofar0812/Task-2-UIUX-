# Task-2-UIUX-
Responsive Webpage Project
 This project demonstrates a responsive webpage using HTML, CSS, and JavaScript. It includes:- A responsive navigation bar with a hamburger menu for small screens.- A flexible hero section with image and text.- Responsive cards using CSS Grid/Flexbox.- Media queries for screen adaptability.- JavaScript for menu toggle.
 Below are the source code files used in the project

# index.html
 <!DOCTYPE html>
 <html lang="en">
 <head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Responsive Webpage</title>
  <link rel="stylesheet" href="style.css" />
 </head>
 <body>
  <header>
    <nav class="navbar">
      <div class="logo">MySite</div>
      <ul class="nav-links" id="navLinks">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
      <div class="hamburger" id="hamburger">&#9776;</div>
    </nav>
  </header>
  <section class="hero">
    <div class="hero-text">
      <h1>Responsive Design</h1>
      <p>This page adapts to any device - mobile, tablet, or desktop!</p>
    </div>
    <div class="hero-image">
      <img src="https://via.placeholder.com/600x300" alt="Hero" />
    </div>
  </section>
  <section class="cards">
    <div class="card">Card 1: Responsive Layout</div>
    <div class="card">Card 2: CSS Grid/Flexbox</div>
    <div class="card">Card 3: Media Queries</div>
  </section>
  <footer>
    <p>&copy; 2025 Responsive Webpage. All rights reserved.</p>
  </footer>
  <script src="script.js"></script>
 </body>
 </html>
style.css
 /* Base styles */
 body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
  line-height: 1.6;
 }
 header {
  background-color: #333;
  color: #fff;
 }
 .navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
 }
 .nav-links {
  display: flex;
  list-style: none;
  gap: 1rem;
 }
 .nav-links li a {
  color: white;
  text-decoration: none;
 }
 .hamburger {
  display: none;
  font-size: 1.5rem;
  cursor: pointer;
 }
 .hero {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  padding: 2rem;
  background: #f4f4f4;
 }
 .hero-text {
  flex: 1;
  padding: 1rem;
 }
 .hero-image {
  flex: 1;
  padding: 1rem;
}
 .hero-image img {
  width: 100%;
  max-width: 100%;
  height: auto;
 }
 .cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1rem;
  padding: 2rem;
 }
 .card {
  background: #ddd;
  padding: 1.5rem;
  border-radius: 8px;
  text-align: center;
 }
 footer {
  background: #333;
  color: white;
  padding: 1rem;
  text-align: center;
 }
 /* Responsive breakpoints */
 @media (max-width: 768px) {
  .nav-links {
    display: none;
    flex-direction: column;
    background: #444;
    position: absolute;
    top: 60px;
    right: 0;
    width: 200px;
  }
  .nav-links.show {
    display: flex;
  }
  .hamburger {
    display: block;
  }
  .hero {
    flex-direction: column;
  }
 }
script.js
 const hamburger = document.getElementById('hamburger');
 const navLinks = document.getElementById('navLinks');
 hamburger.addEventListener('click', () => {
  navLinks.classList.toggle('show');
 })
