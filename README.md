
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CyberAlerta - Conciencia sobre Hackeos</title>
    <link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #fd7575;
            --secondary: #008f11;
            --dark: #0d0208;
            --light: #c8f7c5;
        }
        
        body {
            margin: 0;
            padding: 0;
            font-family: 'Share Tech Mono', monospace;
            color: var(--light);
            background-color: var(--dark);
            overflow-x: hidden;
        }
        
        #world-map {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.3;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 100px 20px;
            position: relative;
            z-index: 1;
        }
        
        h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 3.5rem;
            color: var(--primary);
            text-shadow: 0 0 10px rgba(13, 126, 32, 0.5);
            margin-bottom: 30px;
            animation: pulse 2s infinite;
        }
        
        .subtitle {
            font-size: 1.5rem;
            margin-bottom: 40px;
            line-height: 1.6;
        }
        
        .warning {
            border: 1px solid var(--secondary);
            padding: 20px;
            margin: 40px 0;
            border-radius: 5px;
            background-color: rgba(0, 0, 0, 0.5);
            position: relative;
        }
        
        .warning:before {
            content: "⚠️ ALERTA";
            position: absolute;
            top: -15px;
            left: 20px;
            background-color: var(--dark);
            padding: 0 10px;
            color: var(--primary);
            font-weight: bold;
        }
        
        section {
            margin: 100px 0;
            padding: 40px;
            background-color: rgba(13, 2, 8, 0.8);
            border-left: 3px solid var(--secondary);
            border-radius: 0 5px 5px 0;
        }
        
        h2 {
            color: var(--primary);
            font-family: 'Orbitron', sans-serif;
            font-size: 2.2rem;
            margin-top: 0;
        }
        
        .content-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }
        
        .content-grid img {
            width: 100%;
            border-radius: 5px;
            border: 1px solid var(--secondary);
            box-shadow: 0 0 20px rgba(0, 255, 65, 0.2);
        }
        
        .scroll-down {
            text-align: center;
            margin: 50px 0;
            animation: bounce 2s infinite;
        }
        
        .scroll-down i {
            font-size: 2rem;
            color: var(--primary);
        }
        
        @keyframes pulse {
            0% { text-shadow: 0 0 10px rgba(0, 255, 0, 0.5); }
            50% { text-shadow: 0 0 20px rgba(0, 255, 65, 0.8); }
            100% { text-shadow: 0 0 10px rgba(0, 255, 65, 0.5); }
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-20px); }
            60% { transform: translateY(-10px); }
        }
        
        /* Efectos de terminal */
        .typing {
            border-right: 3px solid var(--primary);
            white-space: nowrap;
            overflow: hidden;
            display: inline-block;
        }
        
        .typing-animation {
            animation: typing 4s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--primary); }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .content-grid {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Mapa mundial animado -->
    <div id="world-map"></div>
    
    <div class="container">
        <header>
            <h1 class="typing typing-animation">CYBER<span style="color: var(--secondary)">ALERTA</span></h1>
            <p class="subtitle">Has llegado aquí por casualidad, pero no es coincidencia que necesites esta información.<br>
            Cada clic en enlaces desconocidos, cada código QR escaneado sin pensar... son puertas que abres a peligros invisibles.</p>
            
            <div class="warning">
                <p>Esta no es una página web común. Aquí aprenderás sobre las amenazas digitales que acechan en cada esquina de internet. 
                Desde ahora, piensa dos veces antes de interactuar con contenido sospechoso.</p>
            </div>
            
            <div class="scroll-down">
                <p>Desplázate para descubrir los peligros</p>
                <i class="fas fa-chevron-down"></i>
            </div>
        </header>
        
        <section id="phishing">
            <div class="content-grid">
                <div>
                    <h2>PHISHING: EL CEBOSO DIGITAL</h2>
                    <p>El phishing es como un pescador lanzando anzuelos en el océano digital. Correos que parecen legítimos, mensajes urgentes de tu "banco", ofertas demasiado buenas para ser verdad... Todo diseñado para que entregues tus datos voluntariamente.</p>
                    <ul>
                        <li>Verifica siempre la URL antes de introducir credenciales</li>
                        <li>Ninguna institución seria te pedirá datos sensibles por email</li>
                        <li>Desconfía de la urgencia ("tu cuenta será cerrada en 24h")</li>
                    </ul>
                </div>
                <img src="https://www.globalsign.com/application/files/9916/8183/6972/Phishing_email_1-min.png" alt="Ejemplo de phishing">
            </div>
        </section>
        
        <section id="malware">
            <div class="content-grid">

                <div>
                    <h2>MALWARE: LOS VIRUS MODERNOS</h2>
                    <p>Desde troyanos que se esconden en software "gratis" hasta ransomware que secuestra tus archivos, el malware evoluciona constantemente. Un simple archivo adjunto o una descarga pirata pueden costarte mucho más de lo que imaginas.</p>
                    <ul>
                        <li>Mantén tu software actualizado</li>
                        <li>Usa un buen antivirus y analiza archivos sospechosos</li>
                        <li>Evita descargas de fuentes no confiables</li>
                        <li>Haz copias de seguridad regularmente</li>
                    </ul>
                </div>
                <img src="https://www.avataracloud.com/wp-content/uploads/2019/09/Trojans.jpg" alt="Tipos de malware">
            </div>
        </section>
        
        <!-- Más secciones sobre otros tipos de ataques -->
        
        <section id="proteccion">
            <h2>ARMADURA DIGITAL: CÓMO PROTEGERTE</h2>
            <div class="content-grid">
                <div>
                    <h3>Contraseñas Seguras</h3>
                    <p>Usa gestores de contraseñas y autenticación de dos factores. Una contraseña única para cada servicio es esencial.</p>
                    
                    <h3>Actualizaciones</h3>
                    <p>Esas molestas actualizaciones parchean vulnerabilidades críticas. No las postergues.</p>
                </div>
                <div>
                    <h3>Conciencia</h3>
                    <p>El eslabón más débil en seguridad eres tú. Educarte es tu mejor defensa.</p>
                    
                    <h3>Redes Seguras</h3>
                    <p>Abrir enlaces desconocidos o escanear códigos sospechosos puede infectar tu dispositivo con virus o exponer tus datos a hackers. Evita riesgos:
                    <p>🔒 No confíes en mensajes u ofertas sospechosas.
🚫 Verifica la fuente antes de interactuar.
📲 Protege tu información personal.</p>

Un momento de precaución puede evitar graves problemas. ¡Cuida tu seguridad digital!</p>
                </div>
            </div>
        </section>
    </div>
    
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    <script>
        // Animación del mapa mundial con Three.js
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
        const renderer = new THREE.WebGLRenderer({ alpha: true });
        renderer.setSize(window.innerWidth, window.innerHeight);
        document.getElementById('world-map').appendChild(renderer.domElement);
        
        // Crear esfera (Tierra)
        const geometry = new THREE.SphereGeometry(5, 32, 32);
        const material = new THREE.MeshBasicMaterial({ 
            color: 0x00ff41,
            wireframe: true 
        });
        const sphere = new THREE.Mesh(geometry, material);
        scene.add(sphere);
        
        camera.position.z = 8;
        
        // Añadir puntos de "ataques"
        const attackPoints = [];
        for (let i = 0; i < 50; i++) {
            const pointGeometry = new THREE.SphereGeometry(0.05, 8, 8);
            const pointMaterial = new THREE.MeshBasicMaterial({ color: 0xff0000 });
            const point = new THREE.Mesh(pointGeometry, pointMaterial);
            
            // Posición aleatoria en la esfera
            const theta = Math.random() * Math.PI * 2;
            const phi = Math.acos(2 * Math.random() - 1);
            const radius = 5.1;
            
            point.position.x = radius * Math.sin(phi) * Math.cos(theta);
            point.position.y = radius * Math.sin(phi) * Math.sin(theta);
            point.position.z = radius * Math.cos(phi);
            
            scene.add(point);
            attackPoints.push({
                mesh: point,
                speed: Math.random() * 0.02 + 0.01,
                direction: new THREE.Vector3(
                    Math.random() - 0.5,
                    Math.random() - 0.5,
                    Math.random() - 0.5
                ).normalize()
            });
        }
        
        // Animación
        function animate() {
            requestAnimationFrame(animate);
            
            sphere.rotation.x += 0.001;
            sphere.rotation.y += 0.002;
            
            // Mover puntos de ataque
            attackPoints.forEach(point => {
                point.mesh.position.addScaledVector(point.direction, point.speed);
                
                // Si el punto se aleja demasiado, reiniciar su posición
                if (point.mesh.position.length() > 7) {
                    const theta = Math.random() * Math.PI * 2;
                    const phi = Math.acos(2 * Math.random() - 1);
                    const radius = 5.1;
                    
                    point.mesh.position.x = radius * Math.sin(phi) * Math.cos(theta);
                    point.mesh.position.y = radius * Math.sin(phi) * Math.sin(theta);
                    point.mesh.position.z = radius * Math.cos(phi);
                }
            });
            
            renderer.render(scene, camera);
        }
        
        animate();
        
        // Ajustar en redimensionamiento
        window.addEventListener('resize', () => {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        });
        
        // Efecto de escritura para otros elementos
        document.addEventListener('DOMContentLoaded', () => {
            const elements = document.querySelectorAll('.typing');
            elements.forEach(el => {
                const text = el.textContent;
                el.textContent = '';
                let i = 0;
                const typing = setInterval(() => {
                    if (i < text.length) {
                        el.textContent += text.charAt(i);
                        i++;
                    } else {
                        clearInterval(typing);
                        el.style.borderRight = 'none';
                    }
                }, 100);
            });
        });
    </script>
</body>
