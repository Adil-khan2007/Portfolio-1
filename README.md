# Portfolio-1
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Portfolio</title>
  <style>
    /* Reset */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: Arial, sans-serif; line-height: 1.6; background: #f5f5f5; color: #333; }

    /* Navbar */
    nav {
      position: fixed; 
      width: 100%; 
      background: #222222; 
      padding: 10px 20px; 
      z-index: 1000;
      display: flex; 
      justify-content: space-between; 
      align-items: center;
    }
    nav a {
      color: #fff; 
      text-decoration: none; 
      margin: 0 15px; 
      transition: color 0.3s;
    }
    nav a:hover { color: #ff9800; }

    /* Sections */
    section { 
      padding: 50px 20px; 
      min-height: 20vh; 
    }
    #home {
      display: flex; 
      justify-content: center; 
      align-items: center; 
      background: linear-gradient(to right, #2196f3, #ff9800); 
      color: white; 
      text-align: center;
      flex-direction: column;
    }
    #home h1 { font-size: 3rem; }
    #home p { margin: 15px 0; font-size: 1.2rem; }
    #home button {
      padding: 10px 20px;
      background: #fff; 
      border: none; 
      cursor: pointer; 
      border-radius: 5px;
      font-size: 1rem;
    }
    #home button:hover { background: #ff9800; color: #fff; }

    /* Skills */
    .skills { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 20px; }
    .skill-box { background: #fff; padding: 20px; border-radius: 8px; text-align: center; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }

    /* Projects */
    .projects { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; }
    .project-card {
      background: #fff; padding: 20px; border-radius: 8px; 
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }
    .project-card:hover { transform: scale(1.05); }

    /* Contact */
    form { max-width: 500px; margin: auto; display: flex; flex-direction: column; }
    input, textarea {
      margin: 10px 0; padding: 10px; border: 1px solid #ccc; border-radius: 5px;
    }
    button { margin-top: 10px; padding: 10px; background: #2196f3; color: #fff; border: none; cursor: pointer; border-radius: 5px; }
    button:hover { background: #ff9800; }

    footer { text-align: center; padding: 20px; background: #222; color: #fff; }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav>
    <div class="logo"><a href="#home">MyPortfolio</a></div>
    <div>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <!-- Home Section -->
  <section id="home">
    <h1>Hello, I'm <span id="typed-name">Md Adil Khan</span></h1>
    <p>Aspiring Web Developer </p>
    <button onclick="scrollToSection('contact')">Hire Me</button>
  </section>

  <!-- About Section -->
  <section id="about">
    <h2>About Me</h2>
    <p>Hi! I'm a passionate web developer who loves creating beautiful and functional websites. I enjoy coding, problem solving, and learning new technologies.</p>
  </section>

  <!-- Skills Section -->
  <section id="skills">
    <h2>My Skills</h2>
    <div class="skills">
      <div class="skill-box">HTML</div>
      <div class="skill-box">CSS</div>
      <div class="skill-box">JavaScript</div>
      <div class="skill-box">Python</div>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects">
    <h2>Projects</h2>
    <div class="projects">
      <div class="project-card">
        <h3>Portfolio Website</h3>
        <p>A personal portfolio built with HTML, CSS, and JavaScript.</p>
      </div>
      <div class="project-card">
        <h3>Zomato Clone</h3>
        <p>A Static Website with the help of HMTL and CSS.</p>
      </div>
      <div class="project-card">
        <h3>Major Project</h3>
        <p>College Management system(for reducing paper work and fast service easily management all the  work without any work load).</p>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <h2>Contact Me</h2>
    
  
  <p>📧 Email: 
     <a href="mailto:yourname@gmail.com">
       ak4786131@gmail.com
     </a>
  </p>
  
  <p>📞 Phone: 
     <a href="tel:+911234567890">+91 8172852165</a>
  </p>
</section>

<form onsubmit="sendMessage(event)">
      <input type="text" id="name" placeholder="Your Name" required>
      <input type="email" id="email" placeholder="Your Email" required>
      <textarea id="message" rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2025 Md Adil Khan. All rights reserved.</p>
  </footer>

  <!-- JavaScript -->
  <script>
    // Smooth scroll
    function scrollToSection(id) {
      document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
    }

    // Contact form handling
    function sendMessage(event) {
      event.preventDefault();
      const name = document.getElementById("name").value;
      const email = document.getElementById("email").value;
      const message = document.getElementById("message").value;

      alert("Thanks " + name + "! Your message has been received.");
      document.querySelector("form").reset();
    }
  </script>

</body>
</html>

