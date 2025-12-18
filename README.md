##INDEX.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Responsive Landing Page</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation Bar -->
    <nav id="navbar">
        <div class="logo">SkillCraft</div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Sections -->
    <section id="home" class="section">Home Section</section>
    <section id="about" class="section">About Section</section>
    <section id="services" class="section">Services Section</section>
    <section id="contact" class="section">Contact Section</section>

    <script src="script.js"></script>
</body>
</html>

 ##STYLE.css
 * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

/* Navbar */
nav {
    position: fixed;
    top: 0;
    width: 100%;
    padding: 15px 30px;
    background-color: transparent;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: 0.3s ease;
    z-index: 1000;
}

nav.scrolled {
    background-color: #111;
}

/* Logo */
.logo {
    font-size: 24px;
    color: white;
    font-weight: bold;
}

/* Nav Links */
.nav-links {
    list-style: none;
    display: flex;
}

.nav-links li {
    margin-left: 20px;
}

.nav-links a {
    text-decoration: none;
    color: white;
    padding: 8px 12px;
    transition: 0.3s;
}

.nav-links a:hover {
    background-color: #00bcd4;
    border-radius: 5px;
}

/* Sections */
.section {
    height: 100vh;
    padding-top: 100px;
    text-align: center;
    font-size: 32px;
}

#home { background: #1abc9c; }
#about { background: #3498db; }
#services { background: #9b59b6; }
#contact { background: #e67e22; }

/* Responsive */
@media (max-width: 768px) {
    .nav-links {
        flex-direction: column;
        background-color: #111;
        position: absolute;
        top: 60px;
        right: 0;
        width: 100%;
        display: none;
    }
}

##SCRIPT.js
window.addEventListener("scroll", function () {
    const navbar = document.getElementById("navbar");

    if (window.scrollY > 50) {
        navbar.classList.add("scrolled");
    } else {
        navbar.classList.remove("scrolled");
    }
});
