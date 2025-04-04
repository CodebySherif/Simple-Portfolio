# Simple-Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Portfolio</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <div class="container">
      <h1>Hi, I'm Sherif 👋</h1>
      <p>Aspiring Front-End Developer</p>
      <button id="toggle-theme">Toggle Dark Mode</button>
    </div>
  </header>

  <section id="about">
    <div class="container">
      <h2>About Me</h2>
      <p>I’m a 3rd-year IT student passionate about building responsive, user-friendly web interfaces. I’ve completed various internships and certifications, and I’m eager to contribute to dynamic development teams.</p>
    </div>
  </section>

  <section id="skills">
    <div class="container">
      <h2>Skills</h2>
      <ul>
        <li>HTML5</li>
        <li>CSS3</li>
        <li>JavaScript</li>
        <li>React (Basic)</li>
        <li>Git & GitHub</li>
      </ul>
    </div>
  </section>

  <section id="projects">
    <div class="container">
      <h2>Projects</h2>
      <div class="project">
        <h3>Burger du Sherif Website</h3>
        <p>A website for my burger brand showcasing menu and ordering info. Built with HTML/CSS/JS.</p>
      </div>
      <div class="project">
        <h3>Milkshake Shop Site</h3>
        <p>A fun, interactive landing page built using vanilla JavaScript for product display.</p>
      </div>
    </div>
  </section>

  <section id="certifications">
    <div class="container">
      <h2>Certifications</h2>
      <ul>
        <li>Python IT Specialist - Certiport</li>
        <li>Full Stack Internship - Ruddo</li>
        <li>Linux - IIT Bombay</li>
        <li>Foundations of UX - Google</li>
      </ul>
    </div>
  </section>

  <section id="contact">
    <div class="container">
      <h2>Contact Me</h2>
      <form id="contactForm">
        <input type="text" id="name" placeholder="Your Name" required />
        <input type="email" id="email" placeholder="Your Email" required />
        <textarea id="message" placeholder="Your Message" required></textarea>
        <button type="submit">Send</button>
      </form>
    </div>
  </section>

  <footer>
    <p>© 2025 Sherif. All rights reserved.</p>
  </footer>

  <script>
    // Theme toggle
    const toggleBtn = document.getElementById('toggle-theme');
    toggleBtn.addEventListener('click', () => {
      document.body.classList.toggle('dark-mode');
    });

    // Contact form validation
    document.getElementById('contactForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();

      if (!name || !email || !message) {
        alert('Please fill in all fields.');
        return;
      }

      alert('Message sent successfully!');
      this.reset();
    });
  </script>

  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #fdfbfb 0%, #ebedee 100%);
      color: #333;
      transition: background 0.3s ease;
    }

    .dark-mode {
      background: linear-gradient(135deg, #1e1e2f 0%, #2a2a40 100%);
      color: #f0f0f0;
    }

    .container {
      width: 90%;
      max-width: 1000px;
      margin: 0 auto;
      padding: 40px 0;
    }

    header {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      text-align: center;
      padding: 40px 0;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    }

    h2 {
      color: #764ba2;
    }

    ul {
      list-style-type: square;
      padding-left: 20px;
    }

    .project {
      background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
      padding: 15px;
      margin-bottom: 10px;
      border-radius: 10px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    input, textarea {
      padding: 12px;
      font-size: 1rem;
      border: 1px solid #ccc;
      border-radius: 10px;
      box-shadow: inset 1px 1px 5px rgba(0,0,0,0.05);
    }

    button {
      padding: 12px;
      font-size: 1rem;
      background: linear-gradient(135deg, #89f7fe 0%, #66a6ff 100%);
      color: #fff;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 5px 15px rgba(102, 166, 255, 0.4);
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    button:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(102, 166, 255, 0.5);
    }

    footer {
      text-align: center;
      padding: 20px;
      background: linear-gradient(135deg, #2a0845 0%, #6441a5 100%);
      color: white;
    }
  </style>
</body>
</html>
