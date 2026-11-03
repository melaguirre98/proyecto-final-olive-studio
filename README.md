# Olive Interior Design Studio

Sitio web estático de un estudio de diseño de interiores en Buenos Aires, desarrollado como proyecto final del curso de Desarrollo Web.

**Sitio desplegado (Netlify):** https://olive-interior-design-studio.netlify.app

## Páginas
- `index.html`: inicio, con galería de proyectos (carousel), servicios y consulta (modal)
- `pages/servicios.html`: servicios y proceso de trabajo (acordeón)
- `pages/proyectos.html`: proyectos realizados
- `pages/sobre-el-estudio.html`: el estudio y sus valores
- `pages/contacto.html`: formulario y datos de contacto

## Tecnologías
HTML5 semántico, SCSS (partials, variables, nesting, mixins con parámetros, `@extend`, `@each` y `@for`), CSS Grid, Flexbox, Bootstrap 5.3 y AOS por CDN, y Git/GitHub.

## Estructura del proyecto
```
index.html
pages/        # servicios, proyectos, sobre-el-estudio y contacto
scss/         # estilos en SCSS (main.scss + partials)
styles/       # CSS compilado (style.css)
assets/       # imágenes y demás contenido multimedia
```

## Estructura de estilos
Todo el CSS propio nace de los archivos `.scss`. `styles/style.css` es solo el resultado de la compilación.

```
scss/
├── main.scss              # único punto de entrada (solo @use)
├── utilities/             # _variables.scss, _mixins.scss
├── base/                  # _tipografia.scss, _base.scss
├── layout/                # _header.scss, _nav.scss, _grid.scss, _footer.scss
└── components/            # _buttons.scss, _cards.scss, _listado.scss, _carousel.scss,
                           # _modal.scss, _accordion.scss, _formulario.scss
```

## Cómo compilar
Con [Sass](https://sass-lang.com/install) instalado (`npm install -g sass`):

```
sass --no-source-map scss/main.scss styles/style.css
```

Para recompilar automáticamente al guardar:

```
sass --watch --no-source-map scss/main.scss:styles/style.css
```
