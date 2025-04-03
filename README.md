<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Viral Pro - Sistemas y Juegos</title>
    <style>
        :root {
            --primary: #3a0ca3;
            --secondary: #4cc9f0;
            --accent: #f72585;
            --background: #111827;
            --text: #f0f2f5;
            --card-bg: #1e293b;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--background);
            color: var(--text);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background-color: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            padding: 15px 0;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            font-size: 24px;
            font-weight: bold;
            color: var(--secondary);
        }
        
        .logo-icon {
            width: 40px;
            height: 40px;
            margin-right: 10px;
            background: linear-gradient(135deg, var(--accent), var(--primary));
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-weight: bold;
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-links a {
            color: var(--text);
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }
        
        .nav-links a:hover {
            color: var(--secondary);
        }
        
        .hero {
            background: linear-gradient(135deg, var(--primary), #240046);
            padding: 150px 0 100px;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            background: linear-gradient(90deg, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .hero p {
            font-size: 20px;
            max-width: 800px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 32px;
            background: linear-gradient(90deg, var(--accent), var(--primary));
            color: white;
            border: none;
            border-radius: 30px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            text-decoration: none;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            font-size: 36px;
            color: var(--secondary);
        }
        
        .history-content, .services-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .card {
            background-color: var(--card-bg);
            border-radius: 15px;
            padding: 30px;
            transition: transform 0.3s;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .card:hover {
            transform: translateY(-10px);
        }
        
        .card h3 {
            color: var(--secondary);
            margin-bottom: 15px;
            font-size: 24px;
        }
        
        .card-icon {
            font-size: 40px;
            margin-bottom: 20px;
            color: var(--accent);
        }
        
        .contact {
            background: linear-gradient(135deg, #240046, var(--primary));
            text-align: center;
        }
        
        .contact-form {
            max-width: 500px;
            margin: 0 auto;
            background-color: var(--card-bg);
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }
        
        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #333;
            border-radius: 8px;
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--text);
            font-size: 16px;
        }
        
        .form-group textarea {
            min-height: 120px;
            resize: vertical;
        }
        
        footer {
            background-color: #0a0a0a;
            text-align: center;
            padding: 30px 0;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        
        .footer-links a {
            color: var(--secondary);
            text-decoration: none;
        }
        
        .footer-links a:hover {
            text-decoration: underline;
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .section-title {
                font-size: 28px;
            }
        }
        
        .glow {
            animation: glow 3s infinite alternate;
        }
        
        @keyframes glow {
            from {
                box-shadow: 0 0 10px var(--secondary);
            }
            to {
                box-shadow: 0 0 20px var(--secondary), 0 0 30px var(--accent);
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <div class="logo-icon">VP</div>
                    <span>Viral Pro</span>
                </div>
                <div class="nav-links">
                    <a href="#inicio">Inicio</a>
                    <a href="#historia">Historia</a>
                    <a href="#servicios">Servicios</a>
                    <a href="#futuro">Futuro</a>
                    <a href="#contacto">Contacto</a>
                </div>
            </nav>
        </div>
    </header>

    <section class="hero" id="inicio">
        <div class="container">
            <h1>VIRAL PRO</h1>
            <p>Desarrollamos sistemas innovadores para tiendas y experiencias de juego extraordinarias.</p>
            <a href="#contacto" class="btn">Contáctanos</a>
        </div>
    </section>

    <section id="historia">
        <div class="container">
            <h2 class="section-title">Nuestra Historia</h2>
            <div class="history-content">
                <div class="card">
                    <div class="card-icon">📅</div>
                    <h3>Nuestros inicios</h3>
                    <p>Viral Pro nació en 2023 con una misión clara: transformar el comercio digital y el entretenimiento con soluciones tecnológicas de vanguardia. Fundada por un equipo de apasionados desarrolladores, nuestra empresa comenzó ofreciendo sistemas para tiendas que revolucionaron la manera en que los negocios gestionan sus operaciones.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🚀</div>
                    <h3>Crecimiento</h3>
                    <p>En poco tiempo, expandimos nuestros horizontes hacia el desarrollo de juegos, uniendo la funcionalidad de nuestros sistemas de gestión con experiencias lúdicas innovadoras. Esta combinación única nos permitió crecer rápidamente y establecernos como referentes en el mercado tecnológico.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🏆</div>
                    <h3>Actualidad</h3>
                    <p>Hoy en 2025, Viral Pro es sinónimo de excelencia e innovación. Nuestro equipo ha crecido y nuestras soluciones han evolucionado, pero mantenemos el mismo espíritu: crear tecnología que mejore la vida de las personas y revolucione los negocios.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="servicios" style="background-color: #1a1a2e;">
        <div class="container">
            <h2 class="section-title">Nuestros Servicios</h2>
            <div class="services-container">
                <div class="card">
                    <div class="card-icon">🛒</div>
                    <h3>Sistemas para Tiendas</h3>
                    <p>Desarrollamos soluciones completas para la gestión de negocios: puntos de venta, inventario, facturación electrónica, CRM y más. Nuestros sistemas son intuitivos, potentes y adaptables a cualquier tipo de comercio.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🎮</div>
                    <h3>Desarrollo de Juegos</h3>
                    <p>Creamos experiencias de juego inmersivas y adictivas para múltiples plataformas. Desde juegos casuales hasta complejas aventuras, combinamos narrativa, diseño y tecnología de vanguardia para ofrecer entretenimiento de calidad.</p>
                </div>
                <div class="card">
                    <div class="card-icon">💼</div>
                    <h3>Soluciones Empresariales</h3>
                    <p>Ofrecemos consultoría tecnológica y desarrollo a medida para empresas que buscan digitalizar sus procesos. Nuestras soluciones optimizan operaciones, reducen costos y mejoran la experiencia de clientes y empleados.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="futuro">
        <div class="container">
            <h2 class="section-title">El Futuro de Viral Pro</h2>
            <div class="card" style="text-align: center; max-width: 800px; margin: 0 auto;">
                <div class="card-icon glow">🤖</div>
                <h3>GPT Viral Pro</h3>
                <p>En 2025, nuestra meta principal es expandir nuestros horizontes en el desarrollo de sistemas de juegos y lanzar nuestra revolucionaria GPT Viral Pro. Esta inteligencia artificial especializada está diseñada para transformar la interacción entre usuarios y sistemas, ofreciendo experiencias personalizadas tanto en comercio como en entretenimiento.</p>
                <p>Nuestra GPT Viral Pro integrará funcionalidades avanzadas de aprendizaje adaptativo, permitiendo que los juegos evolucionen según las preferencias del usuario y que los sistemas comerciales anticipen necesidades de negocios y clientes.</p>
                <p>Estamos en la frontera de una nueva era tecnológica, donde la barrera entre utilidad y entretenimiento se difumina para crear experiencias más completas y satisfactorias.</p>
            </div>
        </div>
    </section>

    <section id="contacto" class="contact">
        <div class="container">
            <h2 class="section-title">Contáctanos</h2>
            <div class="contact-form">
                <form id="email-form">
                    <div class="form-group">
                        <label for="name">Nombre</label>
                        <input type="text" id="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Correo Electrónico</label>
                        <input type="email" id="email" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Mensaje</label>
                        <textarea id="message" required></textarea>
                    </div>
                    <button type="submit" class="btn">Enviar Mensaje</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="logo" style="justify-content: center;">
                    <div class="logo-icon">VP</div>
                    <span>Viral Pro</span>
                </div>
                <p>Sistemas y juegos innovadores desde 2023</p>
                <p>Correo: sviralpro@gmail.com</p>
                <div class="footer-links">
                    <a href="#inicio">Inicio</a>
                    <a href="#historia">Historia</a>
                    <a href="#servicios">Servicios</a>
                    <a href="#futuro">Futuro</a>
                    <a href="#contacto">Contacto</a>
                </div>
                <p>&copy; 2025 Viral Pro. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('email-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;
            
            // En un caso real, aquí enviarías los datos a un servidor
            console.log("Datos del formulario:", {
                nombre: name,
                email: email,
                mensaje: message,
                destinatario: "sviralpro@gmail.com"
            });
            
            // Simulamos el envío exitoso
            alert(`¡Gracias ${name}! Tu mensaje ha sido enviado correctamente. Te contactaremos pronto en ${email}.`);
            
            // Limpiamos el formulario
            this.reset();
        });
        
        // Animación suave para los enlaces de navegación
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
        
        // Detectar el scroll para cambiar el estilo del header
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            
            if (window.scrollY > 50) {
                header.style.backgroundColor = 'rgba(26, 26, 46, 0.95)';
            } else {
                header.style.backgroundColor = 'rgba(0, 0, 0, 0.5)';
            }
        });
    </script>
</body>
</html>
