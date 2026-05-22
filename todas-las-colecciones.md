---
title: "Todas las Colecciones"
layout: page
permalink: /todas-las-colecciones.html
---

<div class="container-fluid my-4" style="padding: 0 2%;">

    <!-- CUADRÍCULA DE COLECCIONES -->
    <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 g-4" id="grid-colecciones">
        
        {% assign todas_colecciones = site.pages | where: "layout", "coleccion" %}
        
        {% for pagina in todas_colecciones %}
        <!-- Añadimos la clase 'tarjeta-coleccion' y ocultamos las que pasen de 10 -->
        <div class="col tarjeta-coleccion" {% if forloop.index > 10 %}style="display: none;"{% endif %}>
            <div class="card h-100" style="border: 4px solid #111111; border-radius: 0; background-color: #ffffff;">
                
                <div style="height: 250px; overflow: hidden; border-bottom: 4px solid #111111;">
                    <img src="{{ pagina.image | relative_url }}" alt="{{ pagina.title }}" style="width: 100%; height: 100%; object-fit: cover;">
                </div>
                
                <div class="card-body d-flex flex-column p-4">
                    <h3 class="card-title" style="font-family: 'Archivo Black', sans-serif; text-transform: uppercase; font-size: 1.5rem; margin-bottom: 1rem;">
                        {{ pagina.title }}
                    </h3>
                    
                    <p class="card-text mb-4" style="font-family: 'Inter', sans-serif; font-size: 1rem;">
                        {% if pagina.description %}
                            {{ pagina.description }}
                        {% else %}
                            {{ pagina.content | strip_html | truncatewords: 20 }}
                        {% endif %}
                    </p>
                    
                    <a href="{{ pagina.url | relative_url }}" class="btn btn-dark mt-auto" style="border-radius: 0; font-family: 'Archivo Black', sans-serif; border: 2px solid #111111; background-color: #111111; color: #ffffff; text-transform: uppercase;">
                        Explorar
                    </a>
                </div>
            </div>
        </div>
        {% endfor %}

    </div>

    <!-- BOTÓN VER MÁS -->
    <!-- Solo se muestra si hay más de 10 colecciones en total -->
    {% if todas_colecciones.size > 10 %}
    <div class="text-end mt-5" id="contenedor-ver-mas">
        <button id="btn-ver-mas" class="btn btn-outline-dark" style="border-radius: 0; font-family: 'Archivo Black', sans-serif; border: 4px solid #111111; text-transform: uppercase; padding: 0.75rem 2.5rem; font-size: 1.2rem;">
            Ver más colecciones &darr;
        </button>
    </div>
    {% endif %}

</div>

<!-- SCRIPT MAGIA PARA EL BOTÓN VER MÁS -->
<script>
document.addEventListener("DOMContentLoaded", function() {
    const btnVerMas = document.getElementById('btn-ver-mas');
    const tarjetas = document.querySelectorAll('.tarjeta-coleccion');
    const contenedorBtn = document.getElementById('contenedor-ver-mas');
    let visibles = 10; // Número de tarjetas que se ven al principio
    let cargarPorClick = 10; // Cuántas tarjetas nuevas aparecen cada vez que pulsas el botón

    if (btnVerMas) {
        btnVerMas.addEventListener('click', function() {
            let mostradasAhora = 0;
            
            // Recorremos las tarjetas y mostramos las siguientes
            for (let i = visibles; i < visibles + cargarPorClick && i < tarjetas.length; i++) {
                tarjetas[i].style.display = 'block';
                mostradasAhora++;
            }
            
            visibles += mostradasAhora;
            
            // Si ya se ven todas, escondemos el botón
            if (visibles >= tarjetas.length) {
                contenedorBtn.style.display = 'none';
            }
        });
    }
});
</script>
