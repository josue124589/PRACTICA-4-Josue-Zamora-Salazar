<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Explora Mundo - Tu Agencia de Viajes</title>
    <style>
        /* Estilos generales */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header */
        header {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1436491865332-7a61a109cc05?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 2rem 0;
            text-align: center;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        nav {
            background-color: #003366;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }
        
        nav ul li {
            margin: 0 1rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        
        nav ul li a:hover {
            background-color: #005588;
        }
        
        .logo {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #ffcc00;
        }
        
        .slogan {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: #ffcc00;
            color: #003366;
            padding: 0.8rem 1.5rem;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #ffdd33;
        }
        
        /* Secciones */
        section {
            padding: 4rem 0;
        }
        
        h2 {
            text-align: center;
            margin-bottom: 2rem;
            color: #003366;
            font-size: 2rem;
        }
        
        /* Paquetes */
        .paquetes {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .paquete {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .paquete:hover {
            transform: translateY(-10px);
        }
        
        .paquete img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .paquete-info {
            padding: 1.5rem;
        }
        
        .paquete-info h3 {
            margin-bottom: 0.5rem;
            color: #003366;
        }
        
        .paquete-info p {
            margin-bottom: 1rem;
            color: #666;
        }
        
        .precio {
            font-weight: bold;
            color: #ff6600;
            font-size: 1.2rem;
        }
        
        /* Formularios */
        .form-container {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            max-width: 800px;
            margin: 0 auto;
        }
        
        form {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }
        
        .form-group {
            margin-bottom: 1rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }
        
        .form-group input, 
        .form-group select, 
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        
        .form-group.full-width {
            grid-column: 1 / -1;
        }
        
        /* Asesoría */
        .asesoria {
            background-color: #003366;
            color: white;
        }
        
        .asesoria h2 {
            color: white;
        }
        
        .asesoria-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            align-items: center;
        }
        
        .asesoria img {
            width: 100%;
            border-radius: 8px;
        }
        
        /* Contacto */
        .contacto-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .contacto-card {
            background-color: white;
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        
        .contacto-card i {
            font-size: 2rem;
            color: #003366;
            margin-bottom: 1rem;
        }
        
        /* Footer */
        footer {
            background-color: #003366;
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
        }
        
        .social-icons {
            margin: 1rem 0;
        }
        
        .social-icons a {
            color: white;
            margin: 0 0.5rem;
            font-size: 1.5rem;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav ul li {
                margin: 0.5rem 0;
            }
            
            .asesoria-content {
                grid-template-columns: 1fr;
            }
            
            form {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Header con navegación -->
    <header>
        <div class="container">
            <h1 class="logo">Explora Mundo</h1>
            <p class="slogan">Descubre los destinos más increíbles con nosotros</p>
            <a href="#reservaciones" class="btn">Reserva Ahora</a>
        </div>
    </header>
    
    <nav>
        <ul>
            <li><a href="#paquetes">Paquetes</a></li>
            <li><a href="#vuelos">Vuelos</a></li>
            <li><a href="#hoteles">Hoteles</a></li>
            <li><a href="#asesoria">Asesoría</a></li>
            <li><a href="#contacto">Contacto</a></li>
        </ul>
    </nav>
    
    <!-- Sección de Paquetes de Viaje -->
    <section id="paquetes" class="container">
        <h2>Paquetes de Viaje</h2>
        <div class="paquetes">
            <div class="paquete">
                <img src="https://images.unsplash.com/photo-1503917988258-f87a78e3c995?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="París">
                <div class="paquete-info">
                    <h3>Romántica París</h3>
                    <p>5 días y 4 noches en la ciudad del amor. Incluye vuelos, hotel 4 estrellas y tours.</p>
                    <p class="precio">$1,299 USD</p>
                    <a href="#reservaciones" class="btn">Reservar</a>
                </div>
            </div>
            
            <div class="paquete">
                <img src="https://images.unsplash.com/photo-1523482580672-f109ba8cb9be?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Cancún">
                <div class="paquete-info">
                    <h3>Paraíso en Cancún</h3>
                    <p>7 días y 6 noches en resort todo incluido. Vuelos, traslados y actividades acuáticas.</p>
                    <p class="precio">$1,599 USD</p>
                    <a href="#reservaciones" class="btn">Reservar</a>
                </div>
            </div>
            
            <div class="paquete">
                <img src="https://images.unsplash.com/photo-1464037866556-6812c9d1c72e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Tokio">
                <div class="paquete-info">
                    <h3>Aventura en Tokio</h3>
                    <p>8 días explorando la cultura japonesa. Vuelos, hotel, guía y transporte local.</p>
                    <p class="precio">$2,499 USD</p>
                    <a href="#reservaciones" class="btn">Reservar</a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Sección de Reservaciones -->
    <section id="reservaciones" class="container">
        <h2>Reserva tu Viaje</h2>
        <div class="form-container">
            <form>
                <div class="form-group">
                    <label for="tipo">Tipo de Reservación</label>
                    <select id="tipo" name="tipo">
                        <option value="paquete">Paquete Completo</option>
                        <option value="vuelo">Solo Vuelo</option>
                        <option value="hotel">Solo Hotel</option>
                        <option value="vuelo-hotel">Vuelo + Hotel</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="destino">Destino</label>
                    <input type="text" id="destino" name="destino" placeholder="¿A dónde viajas?">
                </div>
                
                <div class="form-group">
                    <label for="salida">Fecha de Salida</label>
                    <input type="date" id="salida" name="salida">
                </div>
                
                <div class="form-group">
                    <label for="regreso">Fecha de Regreso</label>
                    <input type="date" id="regreso" name="regreso">
                </div>
                
                <div class="form-group">
                    <label for="adultos">Adultos</label>
                    <input type="number" id="adultos" name="adultos" min="1" value="1">
                </div>
                
                <div class="form-group">
                    <label for="niños">Niños</label>
                    <input type="number" id="niños" name="niños" min="0" value="0">
                </div>
                
                <div class="form-group full-width">
                    <label for="comentarios">Comentarios o Requerimientos Especiales</label>
                    <textarea id="comentarios" name="comentarios" rows="4"></textarea>
                </div>
                
                <div class="form-group full-width">
                    <button type="submit" class="btn">Consultar Disponibilidad</button>
                </div>
            </form>
        </div>
    </section>
    
    <!-- Sección de Vuelos -->
    <section id="vuelos" class="container">
        <h2>Vuelos</h2>
        <div class="form-container">
            <form>
                <div class="form-group">
                    <label for="origen">Origen</label>
                    <input type="text" id="origen" name="origen" placeholder="Ciudad o Aeropuerto">
                </div>
                
                <div class="form-group">
                    <label for="destino-vuelo">Destino</label>
                    <input type="text" id="destino-vuelo" name="destino-vuelo" placeholder="Ciudad o Aeropuerto">
                </div>
                
                <div class="form-group">
                    <label for="fecha-salida">Fecha de Salida</label>
                    <input type="date" id="fecha-salida" name="fecha-salida">
                </div>
                
                <div class="form-group">
                    <label for="fecha-regreso">Fecha de Regreso (Opcional)</label>
                    <input type="date" id="fecha-regreso" name="fecha-regreso">
                </div>
                
                <div class="form-group">
                    <label for="clase">Clase</label>
                    <select id="clase" name="clase">
                        <option value="economica">Económica</option>
                        <option value="premium">Premium Económica</option>
                        <option value="business">Business</option>
                        <option value="primera">Primera Clase</option>
                    </select>
                </div>
                
                <div class="form-group full-width">
                    <button type="submit" class="btn">Buscar Vuelos</button>
                </div>
            </form>
        </div>
    </section>
    
    <!-- Sección de Hoteles -->
    <section id="hoteles" class="container">
        <h2>Hoteles</h2>
        <div class="form-container">
            <form>
                <div class="form-group">
                    <label for="destino-hotel">Destino</label>
                    <input type="text" id="destino-hotel" name="destino-hotel" placeholder="Ciudad, región o hotel">
                </div>
                
                <div class="form-group">
                    <label for="check-in">Check-in</label>
                    <input type="date" id="check-in" name="check-in">
                </div>
                
                <div class="form-group">
                    <label for="check-out">Check-out</label>
                    <input type="date" id="check-out" name="check-out">
                </div>
                
                <div class="form-group">
                    <label for="huespedes">Huéspedes</label>
                    <input type="number" id="huespedes" name="huespedes" min="1" value="1">
                </div>
                
                <div class="form-group">
                    <label for="categoria">Categoría</label>
                    <select id="categoria" name="categoria">
                        <option value="todas">Todas</option>
                        <option value="5">5 Estrellas</option>
                        <option value="4">4 Estrellas</option>
                        <option value="3">3 Estrellas</option>
                    </select>
                </div>
                
                <div class="form-group full-width">
                    <button type="submit" class="btn">Buscar Hoteles</button>
                </div>
            </form>
        </div>
    </section>
    
    <!-- Sección de Asesoría -->
    <section id="asesoria" class="asesoria">
        <div class="container">
            <h2>Asesoría de Viaje Personalizada</h2>
            <div class="asesoria-content">
                <div>
                    <img src="https://images.unsplash.com/photo-1582719471387-9d2f87a1a9c5?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Asesor de viajes">
                </div>
                <div>
                    <p>Nuestros expertos en viajes están listos para ayudarte a planificar la aventura perfecta. Ya sea que necesites:</p>
                    <ul style="margin: 1rem 0 1rem 2rem;">
                        <li>Recomendaciones de destinos</li>
                        <li>Itinerarios personalizados</li>
                        <li>Asesoría en visas y requisitos</li>
                        <li>Seguros de viaje</li>
                        <li>Reservas para grupos</li>
                    </ul>
                    <p>Contáctanos y déjanos crear el viaje de tus sueños.</p>
                    <a href="#contacto" class="btn">Habla con un Asesor</a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Sección de Contacto -->
    <section id="contacto" class="container">
        <h2>Contacto</h2>
        <div class="form-container">
            <form>
                <div class="form-group">
                    <label for="nombre">Nombre</label>
                    <input type="text" id="nombre" name="nombre" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" required>
                </div>
                
                <div class="form-group">
                    <label for="telefono">Teléfono</label>
                    <input type="tel" id="telefono" name="telefono">
                </div>
                
                <div class="form-group full-width">
                    <label for="mensaje">Mensaje</label>
                    <textarea id="mensaje" name="mensaje" rows="5" required></textarea>
                </div>
                
                <div class="form-group full-width">
                    <button type="submit" class="btn">Enviar Mensaje</button>
                </div>
            </form>
        </div>
        
        <div class="contacto-info">
            <div class="contacto-card">
                <i class="fas fa-map-marker-alt"></i>
                <h3>Oficina Central</h3>
                <p>Av. Viajes 1234, Ciudad Turística</p>
            </div>
            
            <div class="contacto-card">
                <i class="fas fa-phone-alt"></i>
                <h3>Teléfono</h3>
                <p>+1 234 567 890</p>
                <p>Lunes a Viernes: 9am - 6pm</p>
            </div>
            
            <div class="contacto-card">
                <i class="fas fa-envelope"></i>
                <h3>Email</h3>
                <p>info@exploramundo.com</p>
                <p>reservaciones@exploramundo.com</p>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <h3>Explora Mundo</h3>
            <p>Tu agencia de viajes de confianza</p>
            
            <div class="social-icons">
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
            </div>
            
            <p>&copy; 2023 Explora Mundo. Todos los derechos reservados.</p>
        </div>
    </footer>
</body>
</html>

