<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Stylish Nav</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    .scrolled {
      background: linear-gradient(to right, #ffffff, #f8f9fa);
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      color: #111;
    }
    .nav-link::after {
      content: '';
      display: block;
      width: 0%;
      height: 2px;
      background: #f59e0b;
      transition: width 0.3s ease-in-out;
    }
    .nav-link:hover::after {
      width: 100%;
    }
  </style>
</head>
<body class="bg-gray-50">


  <!-- 🔷 Stylish Navbar -->
  <nav id="navbar" class="fixed w-full top-0 left-0 z-50 bg-transparent text-white px-8 py-4 flex justify-between items-center transition duration-300">
    <div class="text-3xl font-bold tracking-wide">CreativeZone</div>
    <ul class="flex space-x-8 text-lg">
      <li><a href="#home" class="nav-link relative hover:text-yellow-400 transition">Home</a></li>
      <li><a href="#projects" class="nav-link relative hover:text-yellow-400 transition">Projects</a></li>
      <li><a href="#about" class="nav-link relative hover:text-yellow-400 transition">About</a></li>
      <li><a href="#contact" class="nav-link relative hover:text-yellow-400 transition">Contact</a></li>
    </ul>
  </nav>

  <!-- 🔷 Content Sections -->
  <section id="home" class="h-screen flex items-center justify-center bg-gradient-to-br from-indigo-500 via-purple-500 to-pink-500 text-white pt-24">
    <div class="text-center">
      <h1 class="text-6xl font-bold mb-4">Welcome to CreativeZone</h1>
      <p class="text-xl">We bring elegance to web interfaces 💫</p>
    </div>
  </section>

  <section id="projects" class="py-20 px-6 bg-white text-gray-800">
    <h2 class="text-4xl font-bold mb-6 text-center">Our Projects</h2>
    <p class="text-center text-lg">Explore our interactive interfaces and modern design work.</p>
  </section>

  <section id="about" class="py-20 px-6 bg-gray-100 text-gray-800">
    <h2 class="text-4xl font-bold mb-6 text-center">About Us</h2>
    <p class="text-center text-lg">We’re passionate about building expressive digital experiences.</p>
  </section>

  <section id="contact" class="py-20 px-6 bg-white text-gray-800">
    <h2 class="text-4xl font-bold mb-6 text-center">Get in Touch</h2>
    <p class="text-center text-lg">Follow us or message us — we’d love to hear from you!</p>
  </section>

  <!-- 🔷 Scroll Behavior -->
  <script>
    const navbar = document.getElementById("navbar");
    window.addEventListener("scroll", () => {
      navbar.classList.toggle("scrolled", window.scrollY > 20);
    });
  </script>

</body>
</html>
