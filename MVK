<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Student Portfolio</title>

  <!-- Google Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"/>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      scroll-behavior:smooth;
      font-family:'Poppins',sans-serif;
    }

    body{
      background:#0f172a;
      color:white;
      overflow-x:hidden;
    }

    /* Scrollbar */
    ::-webkit-scrollbar{
      width:10px;
    }

    ::-webkit-scrollbar-thumb{
      background:linear-gradient(#00f5ff,#8b5cf6);
      border-radius:10px;
    }

    /* NAVBAR */
    nav{
      width:100%;
      padding:20px 8%;
      display:flex;
      justify-content:space-between;
      align-items:center;
      position:fixed;
      top:0;
      z-index:1000;
      background:rgba(15,23,42,0.8);
      backdrop-filter:blur(10px);
    }

    nav h1{
      font-size:28px;
      font-weight:700;
      background:linear-gradient(to right,#00f5ff,#8b5cf6);
      -webkit-background-clip:text;
      -webkit-text-fill-color:transparent;
    }

    nav ul{
      display:flex;
      list-style:none;
      gap:30px;
    }

    nav ul li a{
      text-decoration:none;
      color:white;
      transition:0.3s;
      font-weight:500;
    }

    nav ul li a:hover{
      color:#00f5ff;
    }

    /* HERO SECTION */
    .hero{
      min-height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      padding:120px 8%;
      position:relative;
    }

    .hero::before{
      content:'';
      position:absolute;
      width:350px;
      height:350px;
      background:#8b5cf6;
      filter:blur(120px);
      top:50px;
      left:-100px;
      opacity:0.5;
    }

    .hero::after{
      content:'';
      position:absolute;
      width:300px;
      height:300px;
      background:#00f5ff;
      filter:blur(120px);
      bottom:0;
      right:-100px;
      opacity:0.5;
    }

    .hero-content{
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:50px;
      width:100%;
      z-index:1;
      flex-wrap:wrap;
    }

    .hero-text{
      flex:1;
    }

    .hero-text h3{
      color:#00f5ff;
      font-size:22px;
    }

    .hero-text h1{
      font-size:60px;
      margin:10px 0;
    }

    .hero-text h2{
      font-size:32px;
      color:#cbd5e1;
      margin-bottom:20px;
    }

    .hero-text p{
      line-height:1.8;
      color:#cbd5e1;
      margin-bottom:30px;
      max-width:600px;
    }

    .buttons{
      display:flex;
      gap:20px;
      flex-wrap:wrap;
    }

    .btn{
      padding:14px 30px;
      border:none;
      border-radius:30px;
      text-decoration:none;
      color:white;
      font-weight:600;
      transition:0.4s;
      cursor:pointer;
    }

    .btn-primary{
      background:linear-gradient(to right,#00f5ff,#8b5cf6);
    }

    .btn-primary:hover{
      transform:translateY(-5px);
      box-shadow:0 0 20px #00f5ff;
    }

    .btn-secondary{
      border:2px solid #00f5ff;
    }

    .btn-secondary:hover{
      background:#00f5ff;
      color:#0f172a;
    }

    .hero-image{
      flex:1;
      display:flex;
      justify-content:center;
    }

    .hero-image img{
      width:320px;
      height:320px;
      object-fit:cover;
      border-radius:50%;
      border:5px solid #00f5ff;
      box-shadow:0 0 40px #00f5ff;
      animation:float 3s ease-in-out infinite;
    }

    @keyframes float{
      0%{transform:translateY(0);}
      50%{transform:translateY(-15px);}
      100%{transform:translateY(0);}
    }

    /* SECTION */
    section{
      padding:100px 8%;
    }

    .section-title{
      text-align:center;
      font-size:40px;
      margin-bottom:60px;
      position:relative;
    }

    .section-title::after{
      content:'';
      width:100px;
      height:4px;
      background:linear-gradient(to right,#00f5ff,#8b5cf6);
      position:absolute;
      left:50%;
      transform:translateX(-50%);
      bottom:-10px;
      border-radius:10px;
    }

    /* ABOUT */
    .about{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:40px;
      align-items:center;
    }

    .about-card{
      background:rgba(255,255,255,0.05);
      padding:30px;
      border-radius:20px;
      backdrop-filter:blur(10px);
      transition:0.4s;
    }

    .about-card:hover{
      transform:translateY(-10px);
      box-shadow:0 0 20px rgba(0,245,255,0.5);
    }

    /* SKILLS */
    .skills-container{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:25px;
    }

    .skill-box{
      background:rgba(255,255,255,0.05);
      padding:30px;
      border-radius:20px;
      text-align:center;
      transition:0.4s;
    }

    .skill-box:hover{
      transform:scale(1.05);
      background:linear-gradient(to right,#00f5ff22,#8b5cf622);
    }

    .skill-box i{
      font-size:50px;
      margin-bottom:20px;
      color:#00f5ff;
    }

    /* PROJECTS */
    .projects{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
      gap:30px;
    }

    .project-card{
      background:rgba(255,255,255,0.05);
      border-radius:20px;
      overflow:hidden;
      transition:0.4s;
    }

    .project-card:hover{
      transform:translateY(-10px);
      box-shadow:0 0 20px rgba(139,92,246,0.5);
    }

    .project-card img{
      width:100%;
      height:220px;
      object-fit:cover;
    }

    .project-content{
      padding:20px;
    }

    .project-content h3{
      margin-bottom:10px;
    }

    /* CONTACT */
    .contact{
      text-align:center;
    }

    .social-icons{
      margin-top:30px;
      display:flex;
      justify-content:center;
      gap:20px;
    }

    .social-icons a{
      width:55px;
      height:55px;
      display:flex;
      justify-content:center;
      align-items:center;
      border-radius:50%;
      background:rgba(255,255,255,0.08);
      color:white;
      font-size:22px;
      transition:0.4s;
      text-decoration:none;
    }

    .social-icons a:hover{
      background:#00f5ff;
      color:#0f172a;
      transform:rotate(360deg);
    }

    footer{
      text-align:center;
      padding:20px;
      background:#020617;
      color:#94a3b8;
    }

    /* RESPONSIVE */
    @media(max-width:900px){
      .hero-text h1{
        font-size:45px;
      }

      .hero-text h2{
        font-size:25px;
      }

      nav ul{
        display:none;
      }
    }

  </style>
</head>

<body>

  <!-- NAVBAR -->
  <nav>
    <h1>MVK'S PORTFOLIO</h1>

    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section class="hero" id="home">
    <div class="hero-content">

      <div class="hero-text">
        <h3>Hello, I'm</h3>
        <h1>M.Vinay Kumar</h1>
        <h2>BCA Student & Web Developer</h2>

        <p>
          Passionate student focused on creating modern websites,
          creative UI designs, and innovative projects. I enjoy
          coding, designing, and learning new technologies.
        </p>

        <div class="buttons">
          <a href="#" class="btn btn-primary">Download CV</a>
          <a href="#contact" class="btn btn-secondary">Contact Me</a>
        </div>
      </div>

      <div class="hero-image">
        <img src="C:\Users\mvkvi\Downloads\image.jpg" alt="Student">
      </div>

    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <h2 class="section-title">About Me</h2>

    <div class="about">
      <div class="about-card">
        <h3>Who Am I?</h3>
        <p>
          I am a creative and dedicated BCA student interested in web
          development, UI/UX design, and software technologies.
        </p>
      </div>

      <div class="about-card">
        <h3>Education</h3>
        <p>
          Bachelor of Computer Applications (BCA)<br>
          Passionate about programming, innovation, and technology.
        </p>
      </div>

      <div class="about-card">
        <h3>Goals</h3>
        <p>
          My goal is to become a full-stack developer and create impactful
          digital experiences for people around the world.
        </p>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section id="skills">
    <h2 class="section-title">My Skills</h2>

    <div class="skills-container">

      <div class="skill-box">
        <i class="fab fa-html5"></i>
        <h3>HTML5</h3>
      </div>

      <div class="skill-box">
        <i class="fab fa-css3-alt"></i>
        <h3>CSS3</h3>
      </div>

      <div class="skill-box">
        <i class="fab fa-js"></i>
        <h3>JavaScript</h3>
      </div>

      <div class="skill-box">
        <i class="fas fa-database"></i>
        <h3>MySQL</h3>
      </div>

    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects">
    <h2 class="section-title">Projects</h2>

    <div class="projects">

      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1461749280684-dccba630e2f6?q=80&w=1000&auto=format&fit=crop">

        <div class="project-content">
          <h3>Student Management System</h3>
          <p>
            Developed a web application to manage student records and attendance.
          </p>
        </div>
      </div>

      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=1000&auto=format&fit=crop">

        <div class="project-content">
          <h3> Website Design</h3>
          <p>
            Designed a responsive and modern website interface.
          </p>
        </div>
      </div>

      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1000&auto=format&fit=crop">

        <div class="project-content">
          <h3>Portfolio Website</h3>
          <p>
            Built a stylish personal portfolio using HTML, CSS, and JavaScript.
          </p>
        </div>
      </div>

    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <h2 class="section-title">Contact Me</h2>

    <div class="contact">
      <p>Email: Mvkvinay231@gmail.com</p>

    <div class="social-icons">
  <a href="https://www.instagram.com/_404._found/" target="_blank">
    <i class="fab fa-instagram"></i>
  </a>

  <a href="https://www.linkedin.com/in/mvkvinay080" target="_blank">
    <i class="fab fa-linkedin"></i>
  </a>

  <a href="#">
    <i class="fab fa-github"></i>
  </a>

  <a href="#">
    <i class="fab fa-Gmail"></i>
  </a>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    © 2026 Advaith Vinay | Student Portfolio Website
  </footer>

</body>
</html>
