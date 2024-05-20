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








