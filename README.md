# Portafolio responsive — Camilo Jaramillo

## Archivos
- `index.html`: contenido.
- `css/styles.css`: diseño responsive.
- `js/script.js`: menú desplegable para móviles.
- `img/`: carpeta opcional para tu foto.

## Abrir
Abre `index.html` en el navegador o abre la carpeta en VS Code y usa Live Server.

## Personalizar
1. Utilizo mi `Usuario de GitHub`.
2. Utilizo mi `perfil-linkedin`.
3. Utilizo mi `correo real`.
5. Guardo mi foto como `img/camilo-perfil.png` y añade el elemento `<img>` donde prefieras.

El portafolio se adapta a computadores, tabletas y móviles.


## Fotografía de perfil
La foto está guardada en `img/camilo-perfil.png` y se muestra en la sección principal. Para cambiarla, reemplaza ese archivo manteniendo el mismo nombre.


| Tecnología | Responsabilidad |
|---|---|
| HTML5 | Estructura semántica |
| Bootstrap 5.3 | Layout, responsive y componentes |
| CSS3 | Personalización visual |
| JavaScript | Comportamiento proporcionado por Bootstrap |
| Google Fonts | Tipografía |

1. Header y Navbar con Bootstrap 5.3
Comenzaremos con la navegación de tu portafolio.
1. Estructura HTML
Este es el código que ahora tienes en index.html:

<header>
    <nav class="navbar navbar-expand-lg navbar-dark site-navbar"
         aria-label="Navegación principal">

        <div class="container">

            <a class="navbar-brand logo" href="#inicio">
                CJ<span>.</span>
            </a>

            <button
                class="navbar-toggler"
                type="button"
                data-bs-toggle="collapse"
                data-bs-target="#mainNavbar"
                aria-controls="mainNavbar"
                aria-expanded="false"
                aria-label="Abrir o cerrar el menú">

                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="mainNavbar">

                <ul class="navbar-nav ms-auto align-items-lg-center gap-lg-3">

                    <li class="nav-item">
                        <a class="nav-link" href="#sobre-mi">Sobre mí</a>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link" href="#habilidades">Habilidades</a>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link" href="#formacion">Formación</a>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link" href="#proyectos">Proyectos</a>
                    </li>

                    <li class="nav-item">
                        <a class="btn btn-brand btn-sm" href="#contacto">
                            Contacto ↗
                        </a>
                    </li>

                </ul>
            </div>
        </div>
    </nav>
</header>

| Clase | Función |
|---|---|
| `navbar` | Activa el componente de navegación de Bootstrap. |
| `navbar-expand-lg` | Mantiene el menú expandido desde pantallas grandes (992 px). |
| `navbar-dark` | Adapta los colores del menú para fondos oscuros. |
| `container` | Centra el contenido y limita su anchura. |
| `navbar-brand` | Identifica la marca o logotipo. |
| `navbar-toggler` | Crea el botón del menú móvil. |
| `collapse` | Permite ocultar y mostrar el menú. |
| `navbar-collapse` | Aplica el comportamiento de expansión. |
| `navbar-nav` | Da formato a la lista de navegación. |
| `nav-item` | Identifica cada elemento del menú. |
| `nav-link` | Da formato a los enlaces. |
| `ms-auto` | Empuja el menú hacia la derecha. |
| `gap-lg-3` | Agrega separación entre elementos en pantallas grandes. |

<button
    class="navbar-toggler"
    data-bs-toggle="collapse"
    data-bs-target="#mainNavbar">

    Analicemos:

data-bs-toggle="collapse"

Le indica a Bootstrap que el botón controlará un componente desplegable.

data-bs-target="#mainNavbar"

Indica qué elemento HTML debe abrirse o cerrarse.

¿Por qué eliminamos el JavaScript anterior?
Anteriormente tenías:

const button = document.querySelector('.menu-btn');
const links = document.querySelector('.nav-links');

button.addEventListener('click', () => {
    const open = links.classList.toggle('open');
});

Ahora Bootstrap se encarga de esa funcionalidad mediante su componente Collapse.

Para ello utilizamos Bootstrap Bundle:

<script
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.9/dist/js/bootstrap.bundle.min.js"
    crossorigin="anonymous">
</script>

Porque Bootstrap proporciona la estructura y el comportamiento, mientras que nuestro CSS conserva la identidad visual del portafolio.
