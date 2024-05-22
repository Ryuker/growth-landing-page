# Growth Landing Page notes
practise project using plain HTML, CSS and JavaScript

# 1. Setup
- Made folders for `js`, `css` and `assets`
- Added `js/mains.js`
- Added `css/style.css`
- Added `assest/images` and moved images into this folder


# 2. Base HTML and Links
- added `index.html`
- imported stylesheet | `<link rel="stylesheet" href="css/style.css">`
- imported main.js    | `<script src="js/main.js" defer></script>`

## Font - Poppins
- went to google fonts and got the poppins font
- imported into the head tag
``` HTML index.html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css" integrity="sha512-SnH5WK+bZxgPHs44uWIX+LLJAJ9/2PkPKZ5QiAj6Ta86w+fsb2TkcmfRyVX3pBnMFcV7oQPJkl9QevSCWr3W6A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
```

## Icons - FontAwesome
- went to [cdnjs.com](https://cdnjs.com/)

# 3. Navbar HTML
- Added nav element with navbar class
  - contains `logo` and `main-menu`
  - in main menu the login button has a btn class to style it as a button
``` HTML index.html
<nav class="navbar">
  <div class="container">
    <div class="logo">
      <a href="index.html">
        <img src="assets/images/logo.png" alt="logo">
      </a>
    </div>

    <div class="main-menu">
      <ul>
        <li>
          <a href="index.html">Home</a>
        </li>
        <li>
          <a href="#">About Us</a>
        </li>
        <li>
          <a href="#">Blog</a>
        </li>
        <li>
          <a class="btn btn-light" href="#">
            <i class="fas fa-user"></i>Login</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

# 4. Base CSS 
- Added CSS resets
``` CSS style.css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```
## links
``` CSS
a {
  text-decoration: none;
  color: #333;
}
```

## unordered lists
``` CSS
ul {
  list-style: none;
}
```

## Image default size
- specified max-width to be 100%, this prevent it from overflowing the div
``` CSS
img {
  max-width: 100%;
}
```

# 5. Utility CSS Classes

## Container classes
``` CSS
.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 15px;
}

.container-sm {
  max-width: 800px;
  margin: 0 auto;
  padding: 0 15px;
}
```

# 6. Navbar styling
- added flex container inside navbar
``` CSS
/* Navbar */
.navbar {
  background: #fff;
  padding: 20px;
}

.navbar .container {
  display: flex;
  justify-content: space-between;
}
```

## Main menu styling
``` CSS
.navbar .main-menu ul {
  display: flex;
}

.navbar ul li a {
  padding: 10px 20px;
  display: block;
  font-weight: 600;
  transition: 0.5s;
}

.navbar ul li a:hover {
  color: #4891ff;
}
```

## color variables
- added `:root` below the resets
  - this is to scope the variables to be used anywhere
- added `--primary-color: #4891ff;`
- modified `.navbar ul li a:hover` to use the variable for the color | `color: var(--primary-color);`

- added some aditional color variables (see css)

# 7. Button utility classes 
- added button utility class styling
``` CSS
.btn {
  display: inline-block;
  padding: 13px 20px;
  background: var(--light-color);
  color: #333;
  font-weight: 600;
  text-decoration: none;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  transition: 0.5s;
}

.btn:hover {
  opacity: 0.8s;
}

.btn-light{
  background: var(--light-color);
}

.btn-primary{
  background: var(--primary-color);
  color: #fff;
}

.btn-dark {
  background: var(--dark-color);
  color: #fff;
}

.btn-block {
  display: block;
  width: 100%;
}
```

# 8. Navbar changes
- added styling to give the login button a bit more space and space the icon a bit further
``` CSS
.navbar ul li:last-child a {
  margin-left: 10px;
}

.navbar ul li a i {
  margin-right: 10px;
}
```

# 9. Hero Section Elements
- Added HTML for `Hero` section
``` HTML index.html
<!-- Hero -->
<section class="hero">
  <div class="container">
    <div class="hero-content">
      <h1 class="hero-heading text-xxl">
        A powerful solution to grow your startup. Fast!
      </h1>
      <p class="hero-text">
        Organize, collaborate and track progress seamlessly with out one-stop startup growth tool.
      </p>
      <div class="hero-buttons">
        <a href="#" class="btn btn-primary">Get Started</a>
        <a href="#" class="btn btn-light">
          <i class="fas fa-laptop"></i>Book a Demo</a>
      </div>
    </div>
  </div>
</section>
```

# 10. Text Utility Classes
- Added text utility classes for different sizes
``` CSS style.css
/* Text Classes */
.text-xxl {
  font-size: 3rem;  /* 1 rem = 16px */
  line-height: 1.2;
  font-weight: 600;
  margin: 40px 0 20px;
}

.text-xl {
  font-size: 2.2rem;  /* 1 rem = 16px */
  line-height: 1.4;
  font-weight: normal;
  margin: 40px 0 20px;
}

.text-lg {
  font-size: 1.8rem;  /* 1 rem = 16px */
  line-height: 1.4;
  font-weight: normal;
  margin: 30px 0 20px;
}

.text-md {
  font-size: 1.2rem;  /* 1 rem = 16px */
  line-height: 1.4;
  font-weight: normal;
  margin: 20px 0 10px;
}

.text-sm {
  font-size: 0.9rem;  /* 1 rem = 16px */
  line-height: 1.4;
  font-weight: normal;
  margin: 10px 0 5px;
}

.text-center {
  text-align: center;
}
```

# 11. Hero Classes
- Added hero styling
``` CSS
/* Hero */
/* Hero */
.hero {
  margin-bottom: 50px;
}

.hero .container {
  background: url('../assets/images/hero-bg.png') no-repeat;
  background-size: contain;
  background-position: center bottom;
  height: 550px;
}

.hero .hero-content {
  width: 70%;
}

.hero .hero-text {
  width: 70%;
  margin-bottom: 20px;
}
```

# 12. Video Section
- Added HTML for video section
``` HTML index.html
<!-- Video Section -->
<section class="video bg-black">
  <div class="container-sm">
    <h2 class="video-heading text-xl text-center">
      See how it works and get started in less than 2 minutes
    </h2>
    <div class="video-content">
      <a href="#">
        <img class="video-preview" src="assets/images/video-preview.png" alt="video" />
      </a>

      <a href="#" class="btn btn-primary">Get Started</a>
    </div>
  </div>
</section>
```

## Video Section Styling
``` CSS
/* Video */
.video {
  padding: 10px 0 40px;
}

.video-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}
```

# 13. Background Utility Classes
- Added background utility classes
``` CSS
/* Background */
.bg-primary {
  background: var(--primary-color);
  color: #fff;
}

.bg-light {
  background: var(--light-color);
  color: #333;
}

.bg-dark {
  background: var(--dark-color);
  color: #fff;
}

.bg-black {
  background: #000;
  color: #fff;
}
```

# 14. Testimonials Section
- Added testimationals section element
- Added card element and duplicated it several times

## Card Utility Styling
- Added card utility styling
``` CSS
/* Card */
.card {
  background: #fff;
  color: #000;
  border-radius: 20px;
  padding: 20px;
}
```

## Testimonials Styling
- Added testimonials styling
  - using grid for spacing the cards
``` CSS
/* Testimonials */
.testimonials {
  padding: 40px 0;
}

.testimonials .testimonials-heading {
  width: 700px;
  margin-bottom: 40px;
}

.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}

.testimonials .card p:nth-child(2) {
  margin-top: 30px;
  font-weight: bold;
}
```

# 15. Pricing Section
- Added pricing card html elements

## Pricing card styling
- added pricing section styling
``` CSS
/* Pricing */
.pricing-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  margin-top: 50px;
  gap: 30px;
}

.pricing .pricing-card-subheading {
  margin-bottom: 30px;
}

.pricing .pricing-card-price {
  margin-bottom: 30px;
  padding: 20px 0;
  border-bottom: 1px solid #CCC;
}

.pricing ul {
  margin: 30px 0;
}

.pricing ul li {
  margin-bottom: 20px;
}

.pricing ul li i {
  margin-right: 10px;
}

.pricing .pricing-footer {
  margin: 30px;
}
```
- modified `.btn` to use `text-align: center`

# 16. FAQ 
## HTML
- added FAQ Section HTML elements
  - Added a few divs using a group class
  - we'll use javascript to open and close these divs

## CSS
- added FAQ styling classes
  - the `faq-group-header` has `position: relative` so we can absolute position the icon
  - `faq-group-body` is set to `display: none` by default.
    - we'll add a open class to this using JavaScript
``` CSS
.faq {
  padding: 40px 0;
}

.faq .faq-group {
  border-bottom: 1px solid #CCC;
  padding-bottom: 20px;
}

.faq .faq-group .faq-group-header {
  padding: 20px 0;
  margin-bottom: 15px;
  position: relative;
}

.faq .faq-group .faq-group-header h4 {
  font-weight: 600;
  width: 95%;
}

.faq .faq-group .faq-group-header i {
  position: absolute;
  right: 0;
  top: 35px;
  font-size: 1.3rem;
  cursor: pointer;
} 

.faq .faq-group .faq-group-body {
  display: none;
}

.faq .faq-group .faq-group-body.open {
  display: block;
}
```

**FAQ Menu Styling**
``` CSS
.faq ul.faq-menu {
  max-width: 400px;
  margin: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #ddd;
  padding: 10px 20px;
  border-radius: 10px;
  font-weight: 600;
  cursor: pointer;
}

.faq ul.faq-menu li {
  padding: 10px 20px;
  border-radius: 5px;
  text-align: center;
}

.faq ul.faq-menu li.active {
  background: var(--primary-color);
  color: #fff;
}
```

## JavaScript
- Added FAQ Accordion functionality
  - because we set defer on the script import in index.html we don't need to run this in a callback of DOMContentLoaded
  - we basically attach a listener to .faq-content
    - this way clicking on any of it's elements will delegate the event to the top element
    - we then isolate which kind of element we're clicking and toggle the icon appearance and group-body visibility
    - when we toggle visibility of one group-body we hide the visibility of the other group-bodies.
      - this is optional. We can disable this if we want multiple accordions to remain open
    - the icon appearance is also toggled.
``` JS main.js
// FAQ Accordion
const faqContainer = document.querySelector('.faq-content');
faqContainer.addEventListener('click', (e) => {
  const groupHeader = e.target.closest('.faq-group-header');
  
  if (!groupHeader) return;

  const group = groupHeader.parentElement;
  const groupBody = group.querySelector('.faq-group-body');
  const icon = groupHeader.querySelector('i');

  // Toggle Icon
  icon.classList.toggle('fa-plus');
  icon.classList.toggle('fa-minus');

  // Toggle visibility of body
  groupBody.classList.toggle('open');

  // Close other open FAQ bodies
  const otherGroups = faqContainer.querySelectorAll('.faq-group');
  otherGroups.forEach(otherGroup => {
    if (otherGroup !== group) {
      const otherGroupBody = otherGroup.querySelector('.faq-group-body');
      const otherIcon = otherGroup.querySelector('.faq-group-header i');

      otherGroupBody.classList.remove('open');
      otherIcon.classList.remove('fa-minus');
      otherIcon.classList.add('fa-plus');
    }
  });
});
```

# 17. Footer 
## HTML
- Added Footer html elements
``` HTML
<!-- Footer -->
<footer class="footer bg-black">
  <div class="container">
    <div class="footer-grid">
      <div>
        <a href="index.html">
          <img src="assets/images/logo-white.png" alt="logo" />
        </a>
        <div class="card">
          <h4>Subscribe to Newsletter</h4>
          <p class="text-sm">
            Subscribe now to receive tips on how to take your business to the next level.
          </p>
          <form>
            <input type="email" id="email" placeholder="Enter your email" />
            <button type="submit" class="btn btn-primary btn-block">Subscribe</button>
          </form>
        </div>
        <i class="fab fa-linkedin"></i>
        <i class="fab fa-twitter"></i>
      </div>
      <div>
        <h4>Company</h4>
        <ul>
          <li><a href="#">About Us</a></li>
          <li><a href="#">Our Process</a></li>
          <li><a href="#">Join Our Team</a></li>
        </ul>
      </div>
      <div>
        <h4>Resources</h4>
        <ul>
          <li><a href="#">News</a></li>
          <li><a href="#">Research</a></li>
          <li><a href="#">Recent Projects</a></li>
        </ul>
      </div>
      <div>
        <h4>Contact</h4>
        <ul>
          <li><a href="#">hello@growthapp.com</a></li>
        </ul>
      </div>
    </div>
  </div>
</footer>
```

## Styling
- Added footer styling
``` CSS
/* Footer */
.footer {
  padding: 40px 0;
}

.footer h4 {
  margin-bottom: 10px;
}

.footer ul li {
  line-height: 2.5;
}

.footer a {
  color: #ccc;
}

.footer i {
  font-size: 1.5rem;
  margin-right: 10px;
}

.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 30px;
  justify-content: center;
  align-items: center;
}

.footer .card {
  margin: 20px 30px 30px 0;
}

.footer input[type='email'] {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  margin: 20px 0;
}
```

# 18. Responsive Changes: Navbar Hamburger Menu
## HTML
- Added Hamburger Button elements
- Added Mobile Menu elements
``` HTML
<!-- Hamburger Button -->
<button id="hamburger-button" class="hamburger-button">
  <div class="hamburger-line"></div>
  <div class="hamburger-line"></div>
  <div class="hamburger-line"></div>
</button>

<div class="mobile-menu">
  <ul>
    <li>
      <a href="index.html">Home</a>
    </li>
    <li>
      <a href="#">About Us</a>
    </li>
    <li>
      <a href="#">Blog</a>
    </li>
    <li>
      <a class="btn btn-light" href="#">
        <i class="fas fa-user"></i>Login</a>
    </li>
  </ul>
</div>
```

## CSS













