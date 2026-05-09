<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>NodeForge Industrial</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Inter',sans-serif;
    background:#06111f;
    color:white;
    overflow-x:hidden;
}

/* ===== BACKGROUND ===== */

body::before{
    content:'';
    position:fixed;
    inset:0;
    background:
        radial-gradient(circle at top right, rgba(21,101,255,.18), transparent 30%),
        radial-gradient(circle at bottom left, rgba(21,101,255,.15), transparent 25%),
        linear-gradient(135deg,#02060d,#071423,#081c33);
    z-index:-2;
}

.grid-bg{
    position:fixed;
    inset:0;
    background-image:
        linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
    background-size:40px 40px;
    z-index:-1;
}

/* ===== NAVBAR ===== */

header{
    width:100%;
    padding:20px 8%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    position:fixed;
    top:0;
    z-index:1000;
    backdrop-filter:blur(10px);
    background:rgba(2,6,13,.55);
    border-bottom:1px solid rgba(255,255,255,.05);
}

.logo{
    display:flex;
    align-items:center;
    gap:12px;
}

.logo-icon{
    width:52px;
    height:52px;
    border-radius:14px;
    background:linear-gradient(135deg,#1565FF,#4DA3FF);
    display:flex;
    justify-content:center;
    align-items:center;
    font-weight:800;
    font-size:24px;
}

.logo-text h1{
    font-size:24px;
    line-height:1;
    font-weight:800;
}

.logo-text span{
    color:#1565FF;
}

.logo-text p{
    font-size:11px;
    letter-spacing:3px;
    opacity:.75;
    margin-top:4px;
}

nav{
    display:flex;
    gap:30px;
}

nav a{
    text-decoration:none;
    color:white;
    opacity:.8;
    transition:.3s;
    font-weight:500;
}

nav a:hover{
    color:#1565FF;
    opacity:1;
}

/* ===== HERO ===== */

.hero{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:140px 8% 80px;
    gap:60px;
}

.hero-left{
    flex:1;
}

.tag{
    display:inline-block;
    padding:10px 18px;
    border:1px solid rgba(21,101,255,.35);
    border-radius:999px;
    background:rgba(21,101,255,.12);
    color:#7fb0ff;
    font-size:14px;
    margin-bottom:28px;
}

.hero h2{
    font-size:72px;
    line-height:1.02;
    margin-bottom:24px;
    font-weight:800;
}

.hero h2 span{
    color:#1565FF;
}

.hero p{
    font-size:20px;
    line-height:1.7;
    color:rgba(255,255,255,.72);
    max-width:700px;
    margin-bottom:40px;
}

.hero-buttons{
    display:flex;
    gap:20px;
    flex-wrap:wrap;
}

.btn{
    padding:16px 28px;
    border-radius:14px;
    text-decoration:none;
    font-weight:600;
    transition:.3s;
}

.btn-primary{
    background:#1565FF;
    color:white;
    box-shadow:0 0 25px rgba(21,101,255,.4);
}

.btn-primary:hover{
    transform:translateY(-3px);
}

.btn-secondary{
    border:1px solid rgba(255,255,255,.15);
    color:white;
    background:rgba(255,255,255,.04);
}

.btn-secondary:hover{
    background:rgba(255,255,255,.08);
}

/* ===== HERO RIGHT ===== */

.hero-right{
    flex:1;
    display:flex;
    justify-content:center;
    align-items:center;
    position:relative;
}

.device-card{
    width:520px;
    border-radius:28px;
    overflow:hidden;
    position:relative;
    background:linear-gradient(145deg,#091726,#0f2236);
    border:1px solid rgba(255,255,255,.08);
    box-shadow:
        0 0 80px rgba(21,101,255,.25),
        0 30px 80px rgba(0,0,0,.5);
}

.device-card img{
    width:100%;
    display:block;
    opacity:.95;
}

.glow{
    position:absolute;
    width:240px;
    height:240px;
    background:#1565FF;
    border-radius:50%;
    filter:blur(100px);
    opacity:.25;
    z-index:-1;
}

.glow.one{
    top:-50px;
    right:-40px;
}

.glow.two{
    bottom:-40px;
    left:-40px;
}

/* ===== FEATURES ===== */

.features{
    padding:40px 8% 100px;
}

.section-title{
    text-align:center;
    margin-bottom:60px;
}

.section-title h3{
    font-size:42px;
    margin-bottom:14px;
}

.section-title p{
    color:rgba(255,255,255,.65);
}

.feature-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
    gap:24px;
}

.feature-card{
    background:rgba(255,255,255,.04);
    border:1px solid rgba(255,255,255,.06);
    border-radius:24px;
    padding:32px;
    transition:.35s;
    backdrop-filter:blur(8px);
}

.feature-card:hover{
    transform:translateY(-8px);
    border-color:rgba(21,101,255,.45);
    box-shadow:0 0 30px rgba(21,101,255,.15);
}

.feature-icon{
    width:64px;
    height:64px;
    border-radius:18px;
    background:linear-gradient(135deg,#1565FF,#4DA3FF);
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:28px;
    margin-bottom:22px;
}

.feature-card h4{
    font-size:24px;
    margin-bottom:14px;
}

.feature-card p{
    color:rgba(255,255,255,.7);
    line-height:1.7;
}

/* ===== FOOTER ===== */

footer{
    padding:40px 8%;
    border-top:1px solid rgba(255,255,255,.08);
    display:flex;
    justify-content:space-between;
    flex-wrap:wrap;
    gap:20px;
    color:rgba(255,255,255,.65);
}

/* ===== RESPONSIVE ===== */

@media(max-width:1100px){

    .hero{
        flex-direction:column;
        text-align:center;
        padding-top:160px;
    }

    .hero p{
        margin:auto auto 40px;
    }

    .hero-buttons{
        justify-content:center;
    }

    .hero h2{
        font-size:54px;
    }

    .device-card{
        width:100%;
        max-width:520px;
    }

    nav{
        display:none;
    }

}

@media(max-width:640px){

    .hero h2{
        font-size:42px;
    }

    .section-title h3{
        font-size:32px;
    }

}

</style>
</head>

<body>

<div class="grid-bg"></div>

<header>

    <div class="logo">
        <div class="logo-icon">N</div>

        <div class="logo-text">
            <h1>NODE <span>FORGE</span></h1>
            <p>INDUSTRIAL</p>
        </div>
    </div>

    <nav>
        <a href="#">Inicio</a>
        <a href="#">Soluciones</a>
        <a href="#">Servicios</a>
        <a href="#">IoT Industrial</a>
        <a href="#">Contacto</a>
    </nav>

</header>

<section class="hero">

    <div class="hero-left">

        <div class="tag">
            Soluciones Industriales IoT
        </div>

        <h2>
            Conectamos tu operación.<br>
            <span>Optimizamos tu futuro.</span>
        </h2>

        <p>
            Desarrollamos plataformas y dispositivos industriales
            para monitoreo, automatización y adquisición de datos,
            integrando tecnología confiable, segura y escalable
            para la industria moderna.
        </p>

        <div class="hero-buttons">
            <a href="#" class="btn btn-primary">
                Ver Soluciones
            </a>

            <a href="#" class="btn btn-secondary">
                Solicitar Cotización
            </a>
        </div>

    </div>

    <div class="hero-right">

        <div class="glow one"></div>
        <div class="glow two"></div>

        <div class="device-card">
            <img src="Marketing NodeForge Industrial SAC.png" alt="NodeForge Industrial">
        </div>

    </div>

</section>

<section class="features">

    <div class="section-title">
        <h3>Nuestras Capacidades</h3>
        <p>
            Tecnología industrial enfocada en conectividad, monitoreo y automatización.
        </p>
    </div>

    <div class="feature-grid">

        <div class="feature-card">
            <div class="feature-icon">📡</div>
            <h4>Monitoreo en Tiempo Real</h4>
            <p>
                Supervisión continua de variables industriales con acceso remoto y visualización inteligente.
            </p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">⚙️</div>
            <h4>Integración Industrial</h4>
            <p>
                Compatibilidad con Modbus RTU/TCP, MQTT, Ethernet, WiFi y plataformas SCADA.
            </p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">🔔</div>
            <h4>Alarmas Inteligentes</h4>
            <p>
                Notificaciones automáticas y eventos críticos para reducir tiempos de respuesta.
            </p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">🌐</div>
            <h4>Plataformas Web y API</h4>
            <p>
                Desarrollo de dashboards, APIs y soluciones web industriales personalizadas.
            </p>
        </div>

    </div>

</section>

<footer>

    <div>
        © 2026 NodeForge Industrial SAC
    </div>

    <div>
        Forging Industrial Intelligence
    </div>

</footer>

</body>
</html>
