<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog de Tecnología y Hardware</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            max-width: 800px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #333;
        }
        h2 {
            color: #4CAF50;
        }
        p {
            line-height: 1.6;
        }
        .entry {
            margin-bottom: 20px;
        }
        .button {
            display: inline-block;
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 20px;
        }
        .button:hover {
            background-color: #45a049;
        }
        nav {
            margin-bottom: 20px;
        }
        nav a {
            margin: 0 10px;
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            text-decoration: none;
            border-radius: 5px;
        }
        nav a:hover {
            background-color: #45a049;
        }
        section {
            display: none;
        }
        section.active {
            display: block;
        }
        code {
            background-color: #f4f4f4;
            padding: 5px;
            display: block;
            margin-bottom: 10px;
        }
        img {
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Bienvenido a mi Blog de Tecnología</h1>
        <nav>
            <a href="#cpu" onclick="showSection('cpu')">CPU</a>
            <a href="#git" onclick="showSection('git')">Tutorial sobre Git</a>
        </nav>

        <!-- Sección de CPU -->
        <section id="cpu" class="active">
            <div class="entry">
                <h2>La Importancia de la CPU en los Dispositivos Modernos</h2>
                <p>La CPU, o Unidad Central de Procesamiento, es esencial para cualquier dispositivo que procese información. Como el "cerebro" de una computadora, la CPU interpreta y ejecuta las instrucciones de los programas y coordina el trabajo de otros componentes. Su capacidad de procesar múltiples instrucciones rápidamente es crucial para el rendimiento general de un dispositivo.</p>
                <p>Una CPU moderna tiene múltiples núcleos, lo que significa que puede manejar más de una tarea simultáneamente (conocido como procesamiento en paralelo). Esto es importante en aplicaciones que requieren alta potencia de procesamiento, como la edición de video, la simulación 3D y los videojuegos. Las mejoras tecnológicas también han permitido una mayor eficiencia energética, haciendo posible que dispositivos móviles y laptops manejen tareas complejas sin agotar rápidamente la batería.</p>
            </div>

            <div class="entry">
                <h2>Factores Clave al Elegir una CPU</h2>
                <p>Al seleccionar una CPU, debes tener en cuenta varios factores:</p>
                <ul>
                    <li><strong>Número de núcleos:</strong> Una mayor cantidad de núcleos mejora la capacidad de multitarea.</li>
                    <li><strong>Velocidad de reloj:</strong> Mide la cantidad de ciclos que una CPU puede completar por segundo, lo que afecta directamente la rapidez de las operaciones.</li>
                    <li><strong>Cache:</strong> Almacena datos a los que la CPU accede con frecuencia, mejorando la eficiencia.</li>
                    <li><strong>Consumo energético:</strong> Importante para la eficiencia de laptops y dispositivos móviles.</li>
                </ul>
                <p>Estas características afectan no solo el rendimiento de tu equipo, sino también su durabilidad y capacidad de adaptación a futuras necesidades.</p>
            </div>
        </section>

        <!-- Sección de Tutorial sobre Git -->
        <section id="git">
            <h2>Tutorial sobre Git</h2>
            <p>Git es un sistema de control de versiones que permite rastrear cambios en archivos de código a lo largo del tiempo. Es esencial para cualquier desarrollador moderno, ya que facilita el trabajo en equipo y mantiene un registro claro de las modificaciones en los proyectos.</p>

            <h3>1. Inicialización del Repositorio Local</h3>
            <p>Para iniciar un nuevo proyecto con Git en tu máquina local, utiliza el siguiente comando:</p>
            <code>git init</code>
            <p>Este comando inicializa un repositorio Git en el directorio actual, lo que te permite comenzar a rastrear cambios en los archivos.</p>

            <h3>2. Creación y Uso de Branches</h3>
            <p>Las ramas (branches) en Git permiten trabajar en diferentes características o mejoras sin afectar la rama principal del código (generalmente llamada <code>main</code> o <code>master</code>). Para crear una nueva rama, usa:</p>
            <code>git branch nombre-de-la-rama</code>
            <p>Luego, puedes cambiarte a esa rama con el siguiente comando:</p>
            <code>git checkout nombre-de-la-rama</code>
            <p>Una vez hayas realizado cambios, puedes fusionar esta rama con la rama principal utilizando <code>git merge nombre-de-la-rama</code>, lo que permitirá unir los cambios de ambas ramas.</p>
            <img src="Downloads\create-branch-text.png" alt="Ejemplo de creación de branches en Git"width="100" height="200">

            <h3>3. Conectar con un Repositorio Remoto en GitHub</h3>
            <p>Para subir tu proyecto a GitHub y compartirlo con otros, primero necesitas conectar tu repositorio local a uno remoto. Primero, crea un nuevo repositorio en GitHub, luego utiliza este comando para conectarlo:</p>
            <code>git remote add origin https://github.com/usuario/nombre-del-repositorio.git</code>
            <p>Finalmente, puedes subir tus archivos locales al repositorio remoto con el siguiente comando:</p>
            <code>git push -u origin master</code>
            <img src="path/to/remote-screenshot.png" alt="Conectar un repositorio local con GitHub">

            <h3>Beneficios del Control de Versiones</h3>
            <p>Git no solo te permite rastrear los cambios en tu código, sino que también facilita la colaboración en equipo. Al usar ramas y la posibilidad de realizar "pull requests", puedes revisar el código antes de que se una al proyecto principal. Esto ayuda a reducir errores y asegura la calidad del proyecto.</p>
        </section>
    </div>

    <script>
        function showSection(sectionId) {
            // Oculta todas las secciones
            const sections = document.querySelectorAll('section');
            sections.forEach(section => section.classList.remove('active'));

            // Muestra solo la sección seleccionada
            const selectedSection = document.getElementById(sectionId);
            selectedSection.classList.add('active');
        }
    </script>
</body>
</html>
