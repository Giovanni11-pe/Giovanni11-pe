<?php
// Datos dinámicos (puedes editarlos fácilmente)
$nombre = "GIOVANNI";
$titulo = "Desarrollador de Software";
$telefono = "+51 926 957 431";
$email = "giomm67914@gmail.com";

$perfil = "Egresado de Desarrollo de Software en SENATI, con sólida formación en programación y desarrollo web. Proactivo, responsable y orientado a resultados. Busco seguir creciendo profesionalmente.";

$habilidades = [
    "PHP", "HTML", "CSS", "JavaScript", "Python", "Java",
    "MySQL", "Git", "GitHub", "Figma", "XAMPP"
];

$proyectos = [
    [
        "nombre" => "Sistema de Inventario",
        "descripcion" => "Sistema web con control de stock, CRUD y base de datos en MySQL usando PHP."
    ],
    [
        "nombre" => "Página de Vuelos",
        "descripcion" => "Desarrollo de interfaz web conectada a base de datos para solicitudes de vuelos."
    ],
    [
        "nombre" => "Web Corporativa",
        "descripcion" => "Diseño y desarrollo de página web con HTML, CSS y PHP adaptable a distintos dispositivos."
    ]
];
?>

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portafolio - <?php echo $nombre; ?></title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #0f172a;
            color: white;
        }
        header {
            text-align: center;
            padding: 50px 20px;
        }
        header h1 {
            font-size: 40px;
        }
        .banner {
            width: 100%;
            height: 250px;
            background: #1e293b;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #94a3b8;
        }
        section {
            padding: 40px 20px;
            max-width: 900px;
            margin: auto;
        }
        h2 {
            border-bottom: 2px solid #38bdf8;
            padding-bottom: 10px;
        }
        .skills span {
            display: inline-block;
            background: #38bdf8;
            color: black;
            padding: 8px 12px;
            margin: 5px;
            border-radius: 8px;
        }
        .card {
            background: #1e293b;
            padding: 20px;
            margin-top: 15px;
            border-radius: 10px;
        }
        footer {
            text-align: center;
            padding: 20px;
            background: #020617;
        }
    </style>
</head>
<body>

<header>
    <h1>HOLA, SOY <?php echo $nombre; ?></h1>
    <p><?php echo $titulo; ?></p>
</header>

<div class="banner">
    AQUÍ IRÁ TU IMAGEN / BANNER
</div>

<section>
    <h2>Sobre mí</h2>
    <p><?php echo $perfil; ?></p>
</section>

<section>
    <h2>Habilidades</h2>
    <div class="skills">
        <?php foreach($habilidades as $h){ ?>
            <span><?php echo $h; ?></span>
        <?php } ?>
    </div>
</section>

<section>
    <h2>Proyectos</h2>
    <?php foreach($proyectos as $p){ ?>
        <div class="card">
            <h3><?php echo $p['nombre']; ?></h3>
            <p><?php echo $p['descripcion']; ?></p>
        </div>
    <?php } ?>
</section>

<section>
    <h2>Contacto</h2>
    <p>Teléfono: <?php echo $telefono; ?></p>
    <p>Email: <?php echo $email; ?></p>
</section>

<footer>
    <p>© <?php echo date("Y"); ?> <?php echo $nombre; ?> - Portafolio</p>
</footer>

</body>
</html>
