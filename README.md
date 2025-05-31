<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Portafolio personal de Stefany Renteria y Carol Cabreja, Técnico laboral en seguridad y salud en el trabajo.">
    <meta name="keywords" content="portafolio, seguridad y salud en el trabajo, Stefany Renteria, Carol Cabreja, proyectos, SST">
    <title>Stefany Renteria & Carol Cabreja - Técnico en SST</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">

    <style>
        /* --- Reset y Estilos Globales --- */
        :root {
            --primary-dark: #0A192F; /* Azul marino oscuro profundo */
            --secondary-dark: #172A45; /* Azul marino oscuro ligeramente más claro */
            --accent-color: #64FFDA; /* Verde azulado vibrante / Aqua */
            --light-text: #CCD6F6;   /* Azul grisáceo claro para texto */
            --secondary-light-text: #8892B0; /* Azul grisáceo más oscuro para texto secundario */
            --white: #FFFFFF;
            --background-light: #F0F2F5; /* Un gris muy claro para secciones alternas si se desea */
            --card-background: #1E2D48; /* Un poco más claro que el secundario oscuro para tarjetas */

            --font-primary: 'Montserrat', sans-serif;
            --font-secondary: 'Open Sans', sans-serif;

            --transition-speed: 0.3s;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-secondary);
            background-color: var(--primary-dark);
            color: var(--light-text);
            line-height: 1.6;
            overflow-x: hidden; /* Evitar scroll horizontal */
        }

        .container {
            width: 90%;
            max-width: 1100px;
            margin: 0 auto;
            padding: 60px 0;
        }

        h1, h2, h3, h4 {
            font-family: var(--font-primary);
            color: var(--accent-color);
            margin-bottom: 20px;
        }

        h1 { font-size: 3rem; }
        h2 { font-size: 2.5rem; }
        h3 { font-size: 1.8rem; }
        p { margin-bottom: 15px; color: var(--secondary-light-text); }
        a { color: var(--accent-color); text-decoration: none; }
        a:hover { text-decoration: underline; }

        .btn {
            display: inline-block;
            padding: 12px 25px;
            border-radius: 5px;
            font-family: var(--font-primary);
            font-weight: bold;
            text-decoration: none;
            transition: background-color var(--transition-speed) ease, color var(--transition-speed) ease, transform var(--transition-speed) ease;
            cursor: pointer;
            border: 2px solid var(--accent-color);
        }

        .btn-primary {
            background-color: var(--accent-color);
            color: var(--primary-dark);
        }

        .btn-primary:hover {
            background-color: transparent;
            color: var(--accent-color);
            transform: translateY(-3px);
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--accent-color);
        }

        .btn-secondary:hover {
            background-color: var(--accent-color);
            color: var(--primary-dark);
            transform: translateY(-3px);
        }

        section {
            padding: 80px 0;
            border-bottom: 1px solid var(--secondary-dark);
        }
        section:last-of-type {
            border-bottom: none;
        }

        /* --- Navegación --- */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(10, 25, 47, 0.85); /* primary-dark con transparencia */
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 15px 0;
            transition: top 0.3s;
        }

        .navbar .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0; /* Reset padding for navbar container */
            width: 90%;
            max-width: 1100px;
            margin: 0 auto;
        }

        .nav-logo {
            font-family: var(--font-primary);
            font-size: 1.5rem; /* Ajustado para nombres más largos */
            font-weight: bold;
            color: var(--accent-color);
        }

        .nav-links {
            list-style: none;
            display: flex;
        }

        .nav-links li {
            margin-left: 25px;
        }

        .nav-links a {
            color: var(--light-text);
            font-family: var(--font-primary);
            font-weight: 500;
            padding: 5px 0;
            position: relative;
        }
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: var(--accent-color);
            transition: width var(--transition-speed) ease;
        }
        .nav-links a:hover::after,
        .nav-links a.active::after {
            width: 100%;
        }
        .nav-links a.active {
            color: var(--accent-color);
        }


        .menu-toggle {
            display: none; /* Oculto por defecto, visible en móviles */
            font-size: 1.5rem;
            color: var(--accent-color);
            background: none;
            border: none;
            cursor: pointer;
        }


        /* --- Sección Hero --- */
        #hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px; /* Padding para que no pegue a los bordes en pantallas pequeñas */
            background: linear-gradient(rgba(10, 25, 47, 0.8), rgba(10, 25, 47, 0.9)), url('https://placehold.co/1920x1080/0A192F/172A45?text=Fondo+Seguridad+Laboral') no-repeat center center/cover;
            /* Reemplaza 'https://placehold.co/...' con tu imagen: images/hero-background.jpg */
        }

        #hero h1 {
            font-size: 2.8rem; /* Ajustado para titular largo */
            margin-bottom: 15px;
            color: var(--white);
            max-width: 800px; /* Para que no sea demasiado ancho */
        }

        #hero .hero-name {
            font-size: 2.2rem; /* Ajustado */
            color: var(--accent-color);
            margin-bottom: 10px;
            font-family: var(--font-primary);
        }

        #hero .hero-role {
            font-size: 1.4rem; /* Ajustado */
            color: var(--light-text);
            margin-bottom: 25px;
            font-family: var(--font-secondary);
        }

        #hero .hero-description {
            font-size: 1.1rem;
            max-width: 700px;
            margin: 0 auto 30px auto;
            color: var(--secondary-light-text);
        }

        #hero .hero-buttons .btn {
            margin: 0 10px;
        }

        /* --- Sección Acerca de Mí --- */
        #about .container {
            display: flex;
            align-items: center;
            gap: 40px;
        }

        #about .about-image {
            flex-basis: 35%;
            text-align: center;
        }

        #about .about-image img {
            width: 100%;
            max-width: 300px; /* Ajusta según el tamaño de tu foto */
            height: auto;
            object-fit: cover; /* Para que la imagen se ajuste bien */
            border-radius: 10px;
            border: 3px solid var(--accent-color);
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        #about .about-content {
            flex-basis: 65%;
        }


        /* --- Sección Habilidades --- */
        #skills .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        #skills .skill-category {
            background-color: var(--secondary-dark);
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        #skills .skill-category h3 {
            color: var(--accent-color);
            margin-bottom: 15px;
            border-bottom: 1px solid var(--accent-color);
            padding-bottom: 10px;
        }

        #skills ul {
            list-style: none;
        }

        #skills li {
            margin-bottom: 10px;
            padding-left: 20px;
            position: relative;
            color: var(--secondary-light-text);
        }
        #skills li::before {
            content: '▹'; /* O usa un SVG o FontAwesome icon */
            position: absolute;
            left: 0;
            color: var(--accent-color);
            font-weight: bold;
        }
        
        /* Barra de progreso simple (opcional) */
        .progress-bar-container {
            width: 100%;
            background-color: var(--primary-dark);
            border-radius: 5px;
            margin-top: 5px;
            height: 10px;
        }
        .progress-bar {
            height: 100%;
            background-color: var(--accent-color);
            border-radius: 5px;
            text-align: right;
            line-height: 10px; /* Para alinear texto si se añade */
            color: var(--primary-dark);
            font-size: 0.7rem;
            padding-right: 5px;
        }


        /* --- Sección Experiencia y Educación --- */
        .timeline {
            position: relative;
            max-width: 800px; /* Ajusta según preferencia */
            margin: 0 auto;
        }
        .timeline::after { /* La línea central de la timeline */
            content: '';
            position: absolute;
            width: 3px;
            background-color: var(--accent-color);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -1.5px; /* Mitad del ancho de la línea */
        }

        .timeline-item {
            padding: 10px 40px;
            position: relative;
            background-color: inherit;
            width: 50%;
        }
        /* Círculo en la línea */
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 15px;
            height: 15px;
            right: -7.5px; /* (width / 2) */
            background-color: var(--primary-dark);
            border: 3px solid var(--accent-color);
            top: 20px; /* Ajustar para alinear con el contenido */
            border-radius: 50%;
            z-index: 1;
        }

        /* Items a la izquierda */
        .timeline-item.left {
            left: 0;
        }
        /* Items a la derecha */
        .timeline-item.right {
            left: 50%;
        }
        /* Flechas para los items */
        .timeline-item.left::before { /* Flecha izquierda */
            content: " ";
            height: 0;
            position: absolute;
            top: 22px;
            width: 0;
            z-index: 1;
            right: 30px;
            border: medium solid var(--secondary-dark);
            border-width: 10px 0 10px 10px;
            border-color: transparent transparent transparent var(--secondary-dark);
        }
        .timeline-item.right::before { /* Flecha derecha */
            content: " ";
            height: 0;
            position: absolute;
            top: 22px;
            width: 0;
            z-index: 1;
            left: 30px;
            border: medium solid var(--secondary-dark);
            border-width: 10px 10px 10px 0;
            border-color: transparent var(--secondary-dark) transparent transparent;
        }
        /* Ajustar círculo para items derechos */
        .timeline-item.right::after {
            left: -7.5px;
        }

        .timeline-content {
            padding: 20px 30px;
            background-color: var(--secondary-dark);
            position: relative;
            border-radius: 6px;
            box-shadow: 0 3px 8px rgba(0,0,0,0.15);
        }
        .timeline-content h3 {
            color: var(--light-text);
            font-size: 1.5rem;
        }
        .timeline-content .date {
            font-size: 0.9rem;
            color: var(--accent-color);
            margin-bottom: 5px;
            font-weight: bold;
        }
        .timeline-content ul {
            list-style-type: disc; /* Cambiado de none a disc para visibilidad */
            margin-left: 20px;
            padding-left: 0; /* Asegurar que no haya padding extra */
            color: var(--secondary-light-text);
        }
        .timeline-content ul li {
            margin-bottom: 5px;
        }
        .timeline-content p:not(.date) { /* Para párrafos de descripción en la timeline */
             color: var(--secondary-light-text);
        }


        /* --- Sección Proyectos --- */
        #portfolio .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .project-card {
            background-color: var(--card-background);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: transform var(--transition-speed) ease, box-shadow var(--transition-speed) ease;
            display: flex;
            flex-direction: column;
        }
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }

        .project-card img {
            width: 100%;
            height: 200px; /* Altura fija para las imágenes */
            object-fit: cover; /* Para que la imagen cubra el espacio sin deformarse */
        }

        .project-card-content {
            padding: 20px;
            flex-grow: 1; /* Para que el contenido ocupe el espacio restante */
            display: flex;
            flex-direction: column;
        }
        .project-card-content h3 {
            color: var(--accent-color);
            margin-bottom: 10px;
        }
        .project-card-content .project-tech {
            font-size: 0.9rem;
            color: var(--secondary-light-text);
            margin-bottom: 15px;
            font-style: italic;
        }
        .project-card-content .project-links {
            margin-top: auto; /* Empuja los botones al final */
        }
        .project-card-content .btn {
            margin-right: 10px;
            margin-bottom: 5px; /* Espacio si los botones se apilan */
            font-size: 0.9rem;
            padding: 8px 15px;
        }

        /* --- Sección Contacto --- */
        #contact .container {
            display: flex;
            gap: 40px;
            align-items: flex-start;
        }
        #contact .contact-info {
            flex-basis: 40%;
        }
        #contact .contact-form-container {
            flex-basis: 60%;
        }

        .contact-info h3 {
            margin-bottom: 15px;
        }
        .contact-info p {
            margin-bottom: 10px;
        }
        .contact-info p strong {
            color: var(--light-text);
        }
        .contact-info .social-links a {
            margin-right: 15px;
            font-size: 1.5rem; /* Tamaño de iconos sociales */
            color: var(--accent-color);
            transition: color var(--transition-speed) ease;
        }
        .contact-info .social-links a:hover {
            color: var(--light-text);
        }

        .contact-form .form-group {
            margin-bottom: 20px;
        }
        .contact-form label {
            display: block;
            margin-bottom: 5px;
            color: var(--light-text);
            font-family: var(--font-primary);
        }
        .contact-form input[type="text"],
        .contact-form input[type="email"],
        .contact-form textarea {
            width: 100%;
            padding: 12px;
            border-radius: 5px;
            border: 1px solid var(--secondary-light-text);
            background-color: var(--secondary-dark);
            color: var(--light-text);
            font-family: var(--font-secondary);
        }
        .contact-form input[type="text"]:focus,
        .contact-form input[type="email"]:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: var(--accent-color);
            box-shadow: 0 0 5px var(--accent-color);
        }
        .contact-form textarea {
            min-height: 120px;
            resize: vertical;
        }
        .contact-form .btn-primary {
            width: 100%;
            padding: 15px;
        }

        /* --- Footer --- */
        footer {
            text-align: center;
            padding: 30px 0;
            background-color: var(--secondary-dark);
            color: var(--secondary-light-text);
            font-size: 0.9rem;
        }
        footer p a {
            color: var(--accent-color);
        }

        /* --- Animaciones Sutiles (Ejemplo: Fade-in al hacer scroll) --- */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }


        /* --- Media Queries para Responsividad --- */
        @media (max-width: 992px) { /* Tablets y layouts más pequeños */
            h1 { font-size: 2.5rem; }
            #hero h1 { font-size: 2.5rem; }
            h2 { font-size: 2.2rem; }

            .timeline::after { left: 31px; }
            .timeline-item { width: 100%; padding-left: 70px; padding-right: 25px; }
            .timeline-item.left::before, .timeline-item.right::before {
                left: 60px;
                border: medium solid var(--secondary-dark);
                border-width: 10px 10px 10px 0;
                border-color: transparent var(--secondary-dark) transparent transparent;
            }
            .timeline-item.left::after, .timeline-item.right::after {
                left: 23px; /* Ajuste para el círculo */
            }
            .timeline-item.right { left: 0%; }
        }

        @media (max-width: 768px) { /* Móviles */
            .container { width: 95%; }
            h1 { font-size: 2rem; }
            #hero h1 { font-size: 2.2rem; }
            #hero .hero-name { font-size: 1.8rem; }
            #hero .hero-role { font-size: 1.1rem; }
            h2 { font-size: 1.8rem; }

            .menu-toggle { display: block; /* Mostrar botón de menú */ }
            .nav-links {
                display: none; /* Ocultar links por defecto */
                flex-direction: column;
                width: 100%;
                position: absolute;
                top: 60px; /* Altura de la navbar aprox. */
                left: 0;
                background-color: var(--primary-dark);
                padding: 10px 0;
            }
            .nav-links.active { display: flex; /* Mostrar al hacer clic */ }
            .nav-links li {
                margin: 10px 0;
                text-align: center;
            }

            #about .container {
                flex-direction: column;
                text-align: center;
            }
            #about .about-image img { max-width: 250px; }

            #contact .container {
                flex-direction: column;
            }
            #contact .contact-info, #contact .contact-form-container {
                flex-basis: 100%;
            }
            .contact-info { margin-bottom: 30px; text-align: center;}
            .contact-info .social-links { text-align: center; }
        }

        @media (max-width: 480px) {
            #hero h1 { font-size: 1.8rem; }
            #hero .hero-name { font-size: 1.6rem; }
            #hero .hero-role { font-size: 1rem; }
            #hero .hero-description { font-size: 0.9rem; }
            #hero .hero-buttons .btn {
                display: block;
                margin: 10px auto;
                width: 80%;
            }
            .project-card-content .btn {
                font-size: 0.8rem;
                padding: 8px 12px;
            }
        }

    </style>
</head>
<body>

    <nav class="navbar" id="navbar">
        <div class="container">
            <a href="#hero" class="nav-logo">S. Renteria & C. Cabreja</a> <button class="menu-toggle" id="menu-toggle" aria-label="Abrir menú">
                ☰ </button>
            <ul class="nav-links" id="nav-links">
                <li><a href="#hero" class="active">Inicio</a></li>
                <li><a href="#about">Sobre Mí</a></li>
                <li><a href="#skills">Habilidades</a></li>
                <li><a href="#experience">Experiencia</a></li>
                <li><a href="#education">Educación</a></li>
                <li><a href="#portfolio">Proyectos</a></li>
                <li><a href="#contact">Contacto</a></li>
            </ul>
        </div>
    </nav>

    <section id="hero">
        <h1>Protejo la vida en el trabajo promoviendo una cultura de prevención, compromiso y bienestar laboral</h1>
        <p class="hero-name">Stefany Renteria y Carol Cabreja</p>
        <p class="hero-role">Técnico laboral en seguridad y salud en el trabajo</p>
        <p class="hero-description">
            Prevengo accidentes, reduzco riesgos y fortalezco la cultura de seguridad para proteger la vida y mejorar la productividad.
        </p>
        <div class="hero-buttons">
            <a href="#portfolio" class="btn btn-primary">Ver Mis Proyectos</a>
            <a href="#" class="btn btn-secondary" download>Descargar CV</a> </div>
    </section>

    <section id="about" class="fade-in">
        <div class="container">
            <div class="about-image">
                <img src="image_faec32.jpg" alt="Foto profesional de una persona en un entorno industrial con equipo de seguridad">
            </div>
            <div class="about-content">
                <h2>Sobre Mí</h2>
                <p>
                    Mi trabajo en seguridad ocupacional refleja mi compromiso con el bienestar laboral, me
                    motiva prevenir riesgos, capacitar y mejorar entornos de trabajo.
                </p>
                <p>
                    Soy analítica, responsable y disfruto aportar soluciones que cuidan la vida y fortalecen la
                    cultura de seguridad.
                </p>
                </div>
        </div>
    </section>

    <section id="skills" class="fade-in">
        <div class="container">
            <h2>Mis Habilidades</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>Habilidades Técnicas (Ejemplos)</h3>
                    <ul>
                        <li>Identificación de Peligros (Avanzado)
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 90%;"></div></div>
                        </li>
                        <li>Evaluación de Riesgos (Avanzado)
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 85%;"></div></div>
                        </li>
                        <li>Legislación SST (Intermedio)
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 75%;"></div></div>
                        </li>
                        <li>Investigación de Accidentes (Intermedio)
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 70%;"></div></div>
                        </li>
                        <li>Planes de Emergencia (Avanzado)
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 80%;"></div></div>
                        </li>
                        <li>Capacitación en SST (Avanzado)
                             <div class="progress-bar-container"><div class="progress-bar" style="width: 85%;"></div></div>
                        </li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Herramientas</h3>
                    <ul>
                        <li>Microsoft Excel
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 90%;"></div></div>
                        </li>
                        <li>Power Point
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 85%;"></div></div>
                        </li>
                        <li>Microsoft Word
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 90%;"></div></div>
                        </li>
                        <li>AutoCAD (Básico)
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 50%;"></div></div>
                        </li>
                        <li>SG-SST (Software de Gestión)
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 80%;"></div></div>
                        </li>
                        <li>SIMA/ARL
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 75%;"></div></div>
                        </li>
                        <li>Canva
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 70%;"></div></div>
                        </li>
                        <li>Power BI (Básico)
                            <div class="progress-bar-container"><div class="progress-bar" style="width: 60%;"></div></div>
                        </li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Habilidades Blandas</h3>
                    <ul>
                        <li>Comunicación efectiva</li>
                        <li>Empatía</li>
                        <li>Liderazgo</li>
                        <li>Resolución de problemas</li>
                        <li>Pensamiento crítico</li>
                        <li>Trabajo en equipo</li>
                        <li>Adaptabilidad</li>
                        <li>Organización y planificación</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="experience" class="fade-in">
        <div class="container">
            <h2>Experiencia Laboral</h2>
            <div class="timeline">
                <div class="timeline-item left"> <div class="timeline-content">
                        <h3>Inspector de Seguridad y Salud en el trabajo</h3>
                        <p class="date">Colgate Palmolive | 12/2024 – 05/2025 (Previsto)</p>
                        <p>
                            El Inspector de Seguridad y Salud en el Trabajo se encarga de supervisar que se cumplan las normas de prevención de riesgos laborales en los centros de trabajo. Realiza inspecciones, verifica el uso adecuado de equipos de protección, investiga accidentes, elabora informes técnicos, capacita al personal y asesora en la mejora de condiciones laborales. Además, asegura la correcta implementación del sistema de gestión de seguridad y salud en el trabajo y puede proponer sanciones en caso de incumplimientos.
                        </p>
                    </div>
                </div>
                </div>
        </div>
    </section>

    <section id="education" class="fade-in">
        <div class="container">
            <h2>Formación Académica</h2>
            <div class="timeline">
                <div class="timeline-item left"> <div class="timeline-content">
                        <h3>Técnico Laboral en Seguridad y Salud en el Trabajo</h3>
                        <p class="date">Instituto Politécnico Superior de Occidente | 10/01/2023 – 15/06/2025</p>
                        </div>
                </div>
                 </div>
        </div>
    </section>

    <section id="portfolio" class="fade-in">
        <div class="container">
            <h2>Mis Proyectos</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <img src="https://placehold.co/600x400/172A45/64FFDA?text=Proyecto+VR+SST" alt="Imagen del Proyecto VR SST">
                    <div class="project-card-content">
                        <h3>VR SST</h3>
                        <p>
                            Plataforma web para gestionar Sistemas de Gestión de Seguridad y Salud en el Trabajo (SG-SST), cumpliendo normativa y facilitando control de actividades, riesgos y documentación. Mi rol: Líder de desarrollo backend y analista funcional.
                        </p>
                        <p>
                            Funcionalidades: Registro/seguimiento de incidentes, módulo de inspecciones, agenda de capacitaciones, informes automáticos, gestión documental, panel KPI.
                        </p>
                        <p class="project-tech"><strong>Tecnologías:</strong> [Especificar tecnologías, ej: Python (Django/Flask), React, PostgreSQL, Docker]</p>
                        <div class="project-links">
                            <a href="#" class="btn btn-primary" target="_blank" rel="noopener noreferrer">Ver Proyecto</a>
                            <a href="#" class="btn btn-secondary" target="_blank" rel="noopener noreferrer">Ver Código</a>
                        </div>
                    </div>
                </div>
                </div>
        </div>
    </section>

    <section id="contact" class="fade-in">
        <div class="container">
            <div class="contact-info">
                <h2>Hablemos</h2>
                <p>
                    Estoy siempre abierta a discutir nuevos proyectos, ideas creativas o
                    oportunidades para ser parte de tus visiones. No dudes en contactarme.
                </p>
                <p><strong>Email:</strong> <a href="mailto:Bp_lorenstefany_renteriaobregon@colpal.com">Bp_lorenstefany_renteriaobregon@colpal.com</a></p>
                <div class="social-links">
                    <a href="https://www.linkedin.com/jobs/?originalSubdomain=co" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
                        LIn
                    </a>
                    <a href="https://github.com/Stefanyhhhhs/PortafolioWeb" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
                        GH
                    </a>
                    </div>
            </div>
            <div class="contact-form-container">
                <form action="#" method="POST" class="contact-form"> <div class="form-group">
                        <label for="name">Nombre:</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email:</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="subject">Asunto (Opcional):</label>
                        <input type="text" id="subject" name="subject">
                    </div>
                    <div class="form-group">
                        <label for="message">Mensaje:</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary">Enviar Mensaje</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; <span id="currentYear"></span> Stefany Renteria y Carol Cabreja. Todos los derechos reservados.</p>
        <p>Diseñado con <span style="color: var(--accent-color);">❤</span> e inspirado en la web moderna.</p>
    </footer>

    <script>
        // --- Script para el menú de navegación móvil ---
        const menuToggle = document.getElementById('menu-toggle');
        const navLinks = document.getElementById('nav-links');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            // Cambiar el icono del menú (opcional)
            if (navLinks.classList.contains('active')) {
                menuToggle.innerHTML = '✕'; // Icono de cerrar
                menuToggle.setAttribute('aria-label', 'Cerrar menú');
            } else {
                menuToggle.innerHTML = '☰'; // Icono de hamburguesa
                menuToggle.setAttribute('aria-label', 'Abrir menú');
            }
        });

        // Cerrar menú al hacer clic en un enlace (para SPA)
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                if (navLinks.classList.contains('active')) {
                    navLinks.classList.remove('active');
                    menuToggle.innerHTML = '☰';
                    menuToggle.setAttribute('aria-label', 'Abrir menú');
                }
            });
        });


        // --- Script para resaltar enlace activo en la navegación al hacer scroll ---
        const sections = document.querySelectorAll('section');
        const navLi = document.querySelectorAll('.nav-links li a');
        const navbar = document.getElementById('navbar');
        let lastScrollTop = 0;

        window.addEventListener('scroll', () => {
            let current = '';
            const scrollPosition = window.pageYOffset || document.documentElement.scrollTop;

            // Lógica para ocultar/mostrar navbar al hacer scroll
            if (scrollPosition > lastScrollTop && scrollPosition > navbar.offsetHeight) {
                // Scroll hacia abajo
                navbar.style.top = `-${navbar.offsetHeight}px`;
            } else {
                // Scroll hacia arriba
                navbar.style.top = "0";
            }
            lastScrollTop = scrollPosition <= 0 ? 0 : scrollPosition; // Para Mobile o scroll muy arriba


            sections.forEach(section => {
                const sectionTop = section.offsetTop - navbar.offsetHeight - 50; // Ajuste para la altura del navbar y un offset
                const sectionHeight = section.clientHeight;
                if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
                    current = section.getAttribute('id');
                }
            });
            
            // Si no hay sección activa (ej. al final de la página, o si el cálculo falla),
            // intentar activar la última sección si está cerca del final.
            if (!current) {
                const totalHeight = document.body.scrollHeight;
                const viewportHeight = window.innerHeight;
                if (scrollPosition + viewportHeight >= totalHeight - 100) { // Cerca del final
                    current = sections[sections.length -1].getAttribute('id');
                }
            }


            navLi.forEach(a => {
                a.classList.remove('active');
                if (a.getAttribute('href').substring(1) === current) {
                    a.classList.add('active');
                }
            });

            // Activar 'Inicio' si estamos muy arriba
            if (scrollPosition < sections[0].offsetTop - navbar.offsetHeight - 50) {
                 navLi.forEach(a => a.classList.remove('active'));
                 document.querySelector('.nav-links a[href="#hero"]').classList.add('active');
            }
        });

        // --- Script para animación de fade-in al hacer scroll ---
        const fadeInElements = document.querySelectorAll('.fade-in');

        const observerOptions = {
            root: null, // Relativo al viewport
            rootMargin: '0px',
            threshold: 0.1 // El 10% del elemento debe ser visible
        };

        const observer = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    // Opcional: dejar de observar una vez que es visible
                    // observer.unobserve(entry.target);
                } else {
                    // Opcional: remover la clase si queremos que la animación se repita al scrollear arriba y abajo
                    // entry.target.classList.remove('visible');
                }
            });
        }, observerOptions);

        fadeInElements.forEach(el => {
            observer.observe(el);
        });

        // --- Script para el año actual en el footer ---
        document.getElementById('currentYear').textContent = new Date().getFullYear();

    </script>
</body>
</html>
