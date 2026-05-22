---
title: "Sobre el Proyecto"
layout: page
permalink: /about.html
---

<style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Archivo+Black&display=swap');

    /* CAJAS DE CONTENIDO (Fáciles de editar) */
    .about-box {
        border: 4px solid #111111;
        background-color: #ffffff;
        box-shadow: 8px 8px 0px #111111;
        padding: 2.5rem;
        margin-bottom: 3rem;
    }

    .about-box h2 {
        font-family: 'Archivo Black', sans-serif;
        text-transform: uppercase;
        font-size: 1.8rem;
        border-bottom: 3px solid #111111;
        padding-bottom: 0.5rem;
        margin-bottom: 1.5rem;
        color: #111111;
    }

    .about-text {
        font-family: 'Inter', sans-serif;
        font-size: 1.15rem;
        line-height: 1.6;
        color: #111111;
    }

    .about-text p {
        margin-bottom: 1.5rem;
    }

    /* CAJA DE CRÉDITOS (CollectionBuilder) */
    .credits-box {
        background-color: #111111;
        color: #ffffff;
        padding: 2rem;
        border: 4px solid #111111;
        box-shadow: 8px 8px 0px #cccccc;
    }
    
    .credits-box h3 {
        font-family: 'Archivo Black', sans-serif;
        text-transform: uppercase;
        font-size: 1.5rem;
        color: #ffffff;
        margin-bottom: 1rem;
        border-bottom: 2px solid #ffffff;
        padding-bottom: 0.5rem;
    }

    .credits-box p, .credits-box a {
        font-family: 'Inter', sans-serif;
        color: #ffffff;
        font-size: 1rem;
    }

    .credits-box a {
        font-weight: 900;
        text-decoration: underline;
        text-decoration-thickness: 2px;
    }
    .credits-box a:hover {
        background-color: #ffffff;
        color: #111111;
        text-decoration: none;
    }
</style>

<div class="container-fluid" style="padding: 0 5%; margin-top: 3rem; margin-bottom: 5rem;">

    <div class="row">
        
        <!-- ============================================================== -->
        <!-- COLUMNA IZQUIERDA: NUESTROS TEXTOS   -->
        <!-- ============================================================== -->
        <div class="col-lg-8">
            
            <!-- CAJA 1: SOBRE EL PROYECTO -->
            <div class="about-box">
                <h2>Nuestro Propósito</h2>
                <div class="about-text">
                    
                    <!-- Texto del Proyecto -->
                    
                    <p>Este archivo digital nace con la firme intención de preservar, catalogar y difundir nuestra colección. Aquí podéis escribir varios párrafos explicando la historia del proyecto, su contexto histórico o el valor de los objetos que alberga.</p>
                    
                    <!-- FIN DE LA ZONA DE EDICIÓN -->

                </div>
            </div>

            <!-- CAJA 2: EQUIPO Y CONTACTO -->
            <div class="about-box">
                <h2>Equipo y Contacto</h2>
                <div class="about-text">
                    
                    <!-- DATOS -->
                    
                    <p><strong>Dirección del Archivo:</strong> Nombre y Apellido</p>
                    <p><strong>Catalogación y Metadatos:</strong> Nombre y Apellido</p>
                    <p><strong>Desarrollo y Diseño:</strong> Tu Nombre</p>
                    
                    <p class="mt-4">
                        <strong>Contacto:</strong> 
                        <a href="mailto:correo@ejemplo.com" style="color: #111111; font-weight: 900; text-decoration: underline; text-decoration-thickness: 2px;">correo@ejemplo.com</a>
                    </p>
                    
                    <!-- FIN DE LA ZONA DE EDICIÓN -->

                </div>
            </div>

        </div>

        <!-- ============================================================== -->
        <!-- COLUMNA DERECHA: CRÉDITOS A COLLECTIONBUILDER       -->
        <!-- ============================================================== -->
        <div class="col-lg-4 mt-4 mt-lg-0">
            <div class="credits-box">
                <h3>Tecnología</h3>
                <p>Este sitio ha sido construido utilizando <strong>CollectionBuilder</strong>, un proyecto de código abierto impulsado por bibliotecarios e investigadores de la Universidad de Idaho.</p>
                <p>CollectionBuilder genera arquitecturas digitales estáticas, seguras y ultrarrápidas, garantizando la preservación de los datos históricos a largo plazo mediante metadatos puros (CSV) y metodologías web sostenibles.</p>
                <p><a href="https://collectionbuilder.github.io/" target="_blank">Visitar CollectionBuilder &rarr;</a></p>
            </div>
        </div>

    </div>
</div>
