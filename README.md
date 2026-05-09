<!DOCTYPE html>
<html lang="es">
<head>
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
