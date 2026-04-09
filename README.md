<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sátiro Bar | Coctelería Móvil Premium</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Tailwind Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        satiro: {
                            black: '#0a0a0a',
                            dark: '#171717',
                            gold: '#D4AF37',
                            goldHover: '#B5952F',
                            text: '#E5E5E5'
                        }
                    },
                    fontFamily: {
                        sans: ['Montserrat', 'sans-serif'],
                        serif: ['"Playfair Display"', 'serif'],
                    },
                    backgroundImage: {
                        'hero-pattern': "linear-gradient(to bottom, rgba(10, 10, 10, 0.7), rgba(10, 10, 10, 0.9)), url('https://images.unsplash.com/photo-1514362545857-3bc16c4c7d1b?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80')",
                        'bar-pattern': "linear-gradient(to right, rgba(23, 23, 23, 0.95), rgba(23, 23, 23, 0.95)), url('https://images.unsplash.com/photo-1470337458703-415120146915?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80')",
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Styles */
        body {
            background-color: #0a0a0a;
            color: #E5E5E5;
        }
        
        .glass-effect {
            background: rgba(23, 23, 23, 0.7);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(212, 175, 55, 0.1);
        }

        .gold-gradient-text {
            background: linear-gradient(to right, #D4AF37, #FFF8D6, #D4AF37);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        /* Float WhatsApp Button */
        .float-ws {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background-color: #25d366;
            color: #FFF;
            border-radius: 50px;
            text-align: center;
            font-size: 30px;
            box-shadow: 2px 2px 3px #999;
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        .float-ws:hover {
            transform: scale(1.1);
            background-color: #20b858;
        }
        
        /* Mobile Menu */
        #mobile-menu {
            transition: max-height 0.3s ease-in-out;
            max-height: 0;
            overflow: hidden;
        }
        #mobile-menu.open {
            max-height: 300px;
        }
    </style>
</head>
<body class="font-sans antialiased selection:bg-satiro-gold selection:text-satiro-black">

    <!-- Navigation -->
    <nav id="navbar" class="fixed w-full z-50 transition-all duration-300 bg-transparent py-4">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center">
                <!-- Logo -->
                <div class="flex-shrink-0 flex items-center">
                    <a href="#inicio" class="font-serif text-2xl font-bold tracking-widest text-white">
                        SÁTIRO<span class="text-satiro-gold">BAR</span>
                    </a>
                </div>
                
                <!-- Desktop Menu -->
                <div class="hidden md:flex space-x-8 items-center">
                    <a href="#inicio" class="text-sm font-semibold hover:text-satiro-gold transition-colors">Inicio</a>
                    <a href="#nosotros" class="text-sm font-semibold hover:text-satiro-gold transition-colors">Nosotros</a>
                    <a href="#servicios" class="text-sm font-semibold hover:text-satiro-gold transition-colors">Servicios</a>
                    <a href="#carta" class="text-sm font-semibold hover:text-satiro-gold transition-colors">La Carta</a>
                    <a href="#contacto" class="border border-satiro-gold text-satiro-gold px-5 py-2 rounded hover:bg-satiro-gold hover:text-satiro-black transition-all duration-300 font-semibold text-sm">Reserva Ahora</a>
                </div>

                <!-- Mobile Menu Button -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-white hover:text-satiro-gold focus:outline-none">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu Panel -->
        <div id="mobile-menu" class="md:hidden bg-satiro-dark border-b border-gray-800">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 flex flex-col items-center">
                <a href="#inicio" class="block px-3 py-2 text-base font-medium hover:text-satiro-gold mobile-link">Inicio</a>
                <a href="#nosotros" class="block px-3 py-2 text-base font-medium hover:text-satiro-gold mobile-link">Nosotros</a>
                <a href="#servicios" class="block px-3 py-2 text-base font-medium hover:text-satiro-gold mobile-link">Servicios</a>
                <a href="#carta" class="block px-3 py-2 text-base font-medium hover:text-satiro-gold mobile-link">La Carta</a>
                <a href="#contacto" class="block px-3 py-2 text-base font-medium text-satiro-gold mobile-link">Reserva Ahora</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="inicio" class="relative h-screen flex items-center justify-center bg-hero-pattern bg-cover bg-center bg-no-repeat bg-fixed">
        <div class="text-center px-4 max-w-4xl mx-auto z-10 mt-16">
            <p class="text-satiro-gold font-serif italic text-xl md:text-2xl mb-4">La esencia de la fiesta, donde tú elijas</p>
            <h1 class="text-5xl md:text-7xl font-bold font-serif mb-6 text-white uppercase tracking-wider">
                <span class="gold-gradient-text">Sátiro</span> Bar
            </h1>
            <p class="text-lg md:text-xl text-gray-300 mb-10 max-w-2xl mx-auto font-light">
                Servicio exclusivo de coctelería móvil en Lima. Elevamos tus bodas, eventos corporativos y celebraciones privadas con mixología de autor y un servicio impecable.
            </p>
            <div class="flex flex-col sm:flex-row justify-center gap-4">
                <a href="#contacto" class="bg-satiro-gold text-satiro-black px-8 py-3 rounded font-bold hover:bg-satiro-goldHover transition-all duration-300 shadow-[0_0_15px_rgba(212,175,55,0.4)]">
                    Cotiza tu Evento
                </a>
                <a href="#carta" class="border border-white text-white px-8 py-3 rounded font-bold hover:bg-white hover:text-satiro-black transition-all duration-300">
                    Ver Carta
                </a>
            </div>
        </div>
        
        <!-- Scroll Down Indicator -->
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
            <a href="#nosotros" class="text-white opacity-70 hover:text-satiro-gold hover:opacity-100 transition-all">
                <i class="fas fa-chevron-down text-2xl"></i>
            </a>
        </div>
    </section>

    <!-- Nosotros Section -->
    <section id="nosotros" class="py-20 bg-satiro-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col lg:flex-row items-center gap-12">
                <div class="lg:w-1/2">
                    <img src="https://images.unsplash.com/photo-1575037614876-c38528118940?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Bartender preparando cóctel" class="rounded-lg shadow-2xl border border-gray-800" onerror="this.src='https://via.placeholder.com/800x600/171717/D4AF37?text=Satiro+Bar'">
                </div>
                <div class="lg:w-1/2">
                    <div class="flex items-center gap-4 mb-4">
                        <div class="h-[1px] w-12 bg-satiro-gold"></div>
                        <h3 class="text-satiro-gold uppercase tracking-widest text-sm font-semibold">Nuestra Historia</h3>
                    </div>
                    <h2 class="text-3xl md:text-5xl font-serif font-bold text-white mb-6">Más que bebidas, <br>creamos <span class="text-satiro-gold italic font-normal">experiencias</span>.</h2>
                    <p class="text-gray-400 mb-6 leading-relaxed">
                        Inspirados en la mitología y la celebración, <strong class="text-white">Sátiro Bar</strong> nace de la pasión por la alta coctelería y el deseo de llevar la experiencia de un bar premium a cualquier rincón de Lima.
                    </p>
                    <p class="text-gray-400 mb-8 leading-relaxed">
                        Dirigido por profesionales apasionados, nos encargamos de todo: desde el diseño de la carta personalizada hasta el montaje de nuestra elegante barra móvil. Tú solo preocúpate por disfrutar con tus invitados.
                    </p>
                    
                    <div class="grid grid-cols-2 gap-6">
                        <div>
                            <h4 class="text-4xl font-serif text-satiro-gold mb-2">+500</h4>
                            <p class="text-sm text-gray-500 uppercase tracking-wide">Eventos Realizados</p>
                        </div>
                        <div>
                            <h4 class="text-4xl font-serif text-satiro-gold mb-2">100%</h4>
                            <p class="text-sm text-gray-500 uppercase tracking-wide">Satisfacción</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Servicios Section -->
    <section id="servicios" class="py-20 bg-satiro-dark">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <div class="flex items-center justify-center gap-4 mb-4">
                    <div class="h-[1px] w-12 bg-satiro-gold"></div>
                    <h3 class="text-satiro-gold uppercase tracking-widest text-sm font-semibold">Lo que hacemos</h3>
                    <div class="h-[1px] w-12 bg-satiro-gold"></div>
                </div>
                <h2 class="text-3xl md:text-5xl font-serif font-bold text-white mb-6">Nuestros Servicios</h2>
                <p class="text-gray-400">Adaptamos nuestra barra y menú a las necesidades específicas de tu celebración.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Service 1 -->
                <div class="bg-satiro-black p-8 rounded-lg border border-gray-800 hover:border-satiro-gold transition-colors duration-300 group">
                    <div class="w-16 h-16 bg-satiro-dark rounded-full flex items-center justify-center mb-6 text-satiro-gold group-hover:bg-satiro-gold group-hover:text-satiro-black transition-colors duration-300">
                        <i class="fas fa-glass-cheers text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3 font-serif">Barra Libre para Eventos</h3>
                    <p class="text-gray-400 text-sm leading-relaxed mb-4">
                        Paquetes por horas con consumo ilimitado. Ideal para bodas, cumpleaños y fiestas privadas. Incluye licores premium, insumos frescos y cristalería.
                    </p>
                </div>

                <!-- Service 2 -->
                <div class="bg-satiro-black p-8 rounded-lg border border-gray-800 hover:border-satiro-gold transition-colors duration-300 group">
                    <div class="w-16 h-16 bg-satiro-dark rounded-full flex items-center justify-center mb-6 text-satiro-gold group-hover:bg-satiro-gold group-hover:text-satiro-black transition-colors duration-300">
                        <i class="fas fa-cocktail text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3 font-serif">Coctelería de Autor</h3>
                    <p class="text-gray-400 text-sm leading-relaxed mb-4">
                        Diseñamos una carta de cócteles exclusiva para tu evento, inspirada en tus gustos o en la temática de la celebración. Sorprende a tus invitados.
                    </p>
                </div>

                <!-- Service 3 -->
                <div class="bg-satiro-black p-8 rounded-lg border border-gray-800 hover:border-satiro-gold transition-colors duration-300 group">
                    <div class="w-16 h-16 bg-satiro-dark rounded-full flex items-center justify-center mb-6 text-satiro-gold group-hover:bg-satiro-gold group-hover:text-satiro-black transition-colors duration-300">
                        <i class="fas fa-briefcase text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3 font-serif">Eventos Corporativos</h3>
                    <p class="text-gray-400 text-sm leading-relaxed mb-4">
                        Activaciones de marca, lanzamientos y fiestas de fin de año de empresas. Brindamos un servicio profesional que representará la excelencia de tu compañía.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="carta" class="py-20 bg-bar-pattern bg-cover bg-center relative bg-fixed">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <h2 class="text-4xl md:text-5xl font-serif font-bold text-white mb-4">Nuestra Selección</h2>
                <p class="text-satiro-gold font-serif italic text-xl">Clásicos y creaciones de la casa</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 max-w-4xl mx-auto">
                
                <!-- Category 1 -->
                <div>
                    <h3 class="text-2xl font-serif border-b border-satiro-gold pb-2 mb-6 text-white uppercase tracking-wider">Firma del Sátiro</h3>
                    
                    <div class="space-y-6">
                        <div class="flex justify-between items-baseline">
                            <div>
                                <h4 class="text-lg font-bold text-white">Elixir de Dioniso</h4>
                                <p class="text-sm text-gray-400 italic">Pisco Quebranta, zumo de uva, jarabe de romero, cítricos.</p>
                            </div>
                        </div>
                        
                        <div class="flex justify-between items-baseline">
                            <div>
                                <h4 class="text-lg font-bold text-white">Néctar del Bosque</h4>
                                <p class="text-sm text-gray-400 italic">Gin, frutos rojos machacados, tónica, bitter de lavanda.</p>
                            </div>
                        </div>
                        
                        <div class="flex justify-between items-baseline">
                            <div>
                                <h4 class="text-lg font-bold text-white">Fuego de Olimpo</h4>
                                <p class="text-sm text-gray-400 italic">Mezcal, maracuyá, sirope de ají limo, borde de sal de gusano.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Category 2 -->
                <div>
                    <h3 class="text-2xl font-serif border-b border-satiro-gold pb-2 mb-6 text-white uppercase tracking-wider">Clásicos Infalibles</h3>
                    
                    <div class="space-y-6">
                        <div class="flex justify-between items-baseline">
                            <div>
                                <h4 class="text-lg font-bold text-white">Pisco Sour Premium</h4>
                                <p class="text-sm text-gray-400 italic">Pisco puro, zumo de limón fresco, jarabe de goma, clara, Amargo de Angostura.</p>
                            </div>
                        </div>
                        
                        <div class="flex justify-between items-baseline">
                            <div>
                                <h4 class="text-lg font-bold text-white">Negroni Envejecido</h4>
                                <p class="text-sm text-gray-400 italic">Gin, Campari, Vermouth Rosso, piel de naranja, ahumado en roble.</p>
                            </div>
                        </div>
                        
                        <div class="flex justify-between items-baseline">
                            <div>
                                <h4 class="text-lg font-bold text-white">Moscow Mule</h4>
                                <p class="text-sm text-gray-400 italic">Vodka, cerveza de jengibre artesanal, zumo de lima, menta fresca.</p>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
            
            <div class="text-center mt-12">
                <p class="text-gray-300 text-sm">* Esta es solo una pequeña muestra. Diseñamos la carta perfecta para ti.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contacto" class="py-20 bg-satiro-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col lg:flex-row gap-12 bg-satiro-dark rounded-xl overflow-hidden shadow-2xl border border-gray-800">
                
                <!-- Contact Info -->
                <div class="lg:w-2/5 bg-gradient-to-br from-gray-900 to-black p-10 flex flex-col justify-between relative overflow-hidden">
                    <!-- Decoración fondo -->
                    <i class="fas fa-cocktail absolute -bottom-10 -right-10 text-9xl text-gray-800 opacity-30 transform -rotate-12"></i>
                    
                    <div class="relative z-10">
                        <h2 class="text-3xl font-serif font-bold text-white mb-2">Reserva tu Fecha</h2>
                        <p class="text-gray-400 mb-8">Cuéntanos sobre tu evento y nos pondremos en contacto contigo a la brevedad con una propuesta personalizada.</p>
                        
                        <div class="space-y-6">
                            <div class="flex items-start gap-4">
                                <div class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-satiro-gold shrink-0">
                                    <i class="fas fa-map-marker-alt"></i>
                                </div>
                                <div>
                                    <h4 class="text-white font-semibold mb-1">Ubicación</h4>
                                    <p class="text-gray-400 text-sm">Lima, Perú<br>Atendemos en toda la ciudad y balnearios.</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start gap-4">
                                <div class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-satiro-gold shrink-0">
                                    <i class="fab fa-whatsapp text-lg"></i>
                                </div>
                                <div>
                                    <h4 class="text-white font-semibold mb-1">WhatsApp / Teléfono</h4>
                                    <p class="text-gray-400 text-sm">+51 987 654 321</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start gap-4">
                                <div class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-satiro-gold shrink-0">
                                    <i class="fas fa-envelope"></i>
                                </div>
                                <div>
                                    <h4 class="text-white font-semibold mb-1">Correo Electrónico</h4>
                                    <p class="text-gray-400 text-sm">eventos@satirobar.pe</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Contact Form -->
                <div class="lg:w-3/5 p-10">
                    <form onsubmit="event.preventDefault(); alert('¡Gracias por tu mensaje! En un entorno real, esto enviaría tu solicitud al equipo de Sátiro Bar.');">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">Nombre completo</label>
                                <input type="text" required class="w-full bg-gray-900 border border-gray-700 rounded p-3 text-white focus:outline-none focus:border-satiro-gold focus:ring-1 focus:ring-satiro-gold transition-colors">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">Teléfono / Celular</label>
                                <input type="tel" required class="w-full bg-gray-900 border border-gray-700 rounded p-3 text-white focus:outline-none focus:border-satiro-gold focus:ring-1 focus:ring-satiro-gold transition-colors">
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">Tipo de Evento</label>
                                <select class="w-full bg-gray-900 border border-gray-700 rounded p-3 text-white focus:outline-none focus:border-satiro-gold focus:ring-1 focus:ring-satiro-gold transition-colors appearance-none">
                                    <option>Boda</option>
                                    <option>Cumpleaños / Privado</option>
                                    <option>Corporativo</option>
                                    <option>Otro</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">Fecha Estimada</label>
                                <input type="date" class="w-full bg-gray-900 border border-gray-700 rounded p-3 text-white focus:outline-none focus:border-satiro-gold focus:ring-1 focus:ring-satiro-gold transition-colors [color-scheme:dark]">
                            </div>
                        </div>

                        <div class="mb-6">
                            <label class="block text-sm font-medium text-gray-400 mb-2">N° Estimado de Invitados</label>
                            <input type="number" class="w-full bg-gray-900 border border-gray-700 rounded p-3 text-white focus:outline-none focus:border-satiro-gold focus:ring-1 focus:ring-satiro-gold transition-colors">
                        </div>

                        <div class="mb-6">
                            <label class="block text-sm font-medium text-gray-400 mb-2">Detalles adicionales</label>
                            <textarea rows="4" class="w-full bg-gray-900 border border-gray-700 rounded p-3 text-white focus:outline-none focus:border-satiro-gold focus:ring-1 focus:ring-satiro-gold transition-colors" placeholder="Cuéntanos un poco más sobre lo que tienes en mente..."></textarea>
                        </div>
                        
                        <button type="submit" class="w-full bg-satiro-gold text-satiro-black font-bold py-4 rounded hover:bg-satiro-goldHover transition-colors duration-300 uppercase tracking-widest text-sm">
                            Solicitar Cotización
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-[#050505] pt-16 pb-8 border-t border-gray-900">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center md:items-start gap-8 mb-12 border-b border-gray-800 pb-12">
                <!-- Brand -->
                <div class="text-center md:text-left">
                    <a href="#inicio" class="font-serif text-3xl font-bold tracking-widest text-white inline-block mb-4">
                        SÁTIRO<span class="text-satiro-gold">BAR</span>
                    </a>
                    <p class="text-gray-500 max-w-xs text-sm">Elevando el estándar de la coctelería móvil en Lima. Eventos inolvidables, tragos excepcionales.</p>
                </div>
                
                <!-- Social -->
                <div class="text-center md:text-right">
                    <h4 class="text-white font-semibold mb-4 uppercase tracking-widest text-sm">Síguenos</h4>
                    <div class="flex gap-4 justify-center md:justify-end">
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-900 flex items-center justify-center text-gray-400 hover:bg-satiro-gold hover:text-satiro-black transition-all">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-900 flex items-center justify-center text-gray-400 hover:bg-satiro-gold hover:text-satiro-black transition-all">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-900 flex items-center justify-center text-gray-400 hover:bg-satiro-gold hover:text-satiro-black transition-all">
                            <i class="fab fa-tiktok"></i>
                        </a>
                    </div>
                </div>
            </div>
            
            <div class="flex flex-col md:flex-row justify-between items-center text-sm text-gray-600">
                <p>&copy; 2026 Sátiro Bar. Todos los derechos reservados.</p>
                <p class="mt-2 md:mt-0">Lima, Perú</p>
            </div>
        </div>
    </footer>

    <!-- WhatsApp Floating Button -->
    <a href="https://wa.me/51987654321?text=Hola%20Sátiro%20Bar,%20deseo%20información%20para%20un%20evento" target="_blank" class="float-ws" aria-label="Contactar por WhatsApp">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- Scripts -->
    <script>
        // Navbar Scroll Effect
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('glass-effect', 'py-2');
                navbar.classList.remove('py-4');
            } else {
                navbar.classList.remove('glass-effect', 'py-2');
                navbar.classList.add('py-4');
            }
        });

        // Mobile Menu Toggle
        const btn = document.getElementById('mobile-menu-btn');
        const menu = document.getElementById('mobile-menu');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        btn.addEventListener('click', () => {
            menu.classList.toggle('open');
        });

        // Close mobile menu when clicking a link
        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                menu.classList.remove('open');
            });
        });
    </script>
</body>
</html>
