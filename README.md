# Recetario Karly

Recetario web estático (HTML + CSS puro, sin frameworks) para publicar en
GitHub Pages.

## Estructura

```
recetario/
├── index.html                 # Portada con el índice de recetas
├── css/
│   └── estilos.css            # Paleta, tipografías y componentes visuales
├── recetas/
│   └── 001-cookies-chips.html # Recetas, una por archivo
└── assets/
    └── img/                   # Fotos reales de las recetas (opcional)
```

## Cómo agregar una receta nueva

1. Copia `recetas/001-cookies-chips.html` y renómbralo, por ejemplo
   `recetas/002-nombre-de-tu-receta.html`.
2. Cambia el número, el título, los ingredientes y el procedimiento.
3. Si tienes una foto, agrégala en `assets/img/` y reemplaza el bloque
   `<div class="polaroid__foto">` por una etiqueta `<img>` apuntando a esa
   ruta.
4. En `index.html`, dentro de la sección correspondiente (o creando una
   nueva `<section class="seccion" id="...">` si es otra categoría), agrega
   una tarjeta `<a class="tarjeta" href="recetas/002-....html">` copiando el
   patrón de la tarjeta existente.
5. Si creaste una categoría nueva, añade su enlace en `.indice__lista` del
   `<header>` para que aparezca en el índice de navegación.

## Publicar en GitHub Pages

En la configuración del repositorio (Settings → Pages), selecciona la rama
`main` y la carpeta raíz (`/`) como origen. El sitio quedará disponible en
la URL que GitHub asigne.
