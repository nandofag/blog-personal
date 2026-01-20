# Blog Personal - Preentrega 3 Desarrollo Web

Proyecto de blog personal desarrollado como tercera entrega del curso de Desarrollo Web de Coderhouse.

## Descripción

Sitio web personal que incluye un blog, portfolio de proyectos, información personal y formulario de contacto. Desarrollado con HTML5, CSS3 avanzado, Bootstrap 5 y **SASS/SCSS**.

## Características

- **Diseño Responsive**: Optimizado para todos los dispositivos (mobile-first)
- **Bootstrap 5**: Framework CSS para componentes y sistema de grillas
- **SASS/SCSS**: Preprocesador CSS con arquitectura modular
- **CSS Avanzado**: Variables, animaciones, transiciones y efectos modernos
- **Accesibilidad**: Cumple con estándares de accesibilidad web
- **SEO Optimizado**: Meta tags y estructura semántica

## Tecnologías Utilizadas

- HTML5
- CSS3 (Flexbox, Grid, Animaciones)
- **SASS/SCSS** (Variables, Mixins, Nesting, @extend, @each, @for)
- Bootstrap 5.3.2
- Bootstrap Icons
- Node.js (para compilación de SASS)

## Estructura del Proyecto

```
blog-personal/
├── css/
│   └── styles.css          # CSS compilado desde SCSS
├── scss/                   # Archivos fuente SASS
│   ├── abstracts/
│   │   ├── _variables.scss # Variables SASS
│   │   ├── _mixins.scss    # Mixins reutilizables
│   │   ├── _functions.scss # Funciones SASS
│   │   └── _index.scss
│   ├── base/
│   │   ├── _reset.scss     # Reset y estilos base
│   │   ├── _typography.scss# Tipografía
│   │   └── _index.scss
│   ├── components/
│   │   ├── _buttons.scss   # Estilos de botones
│   │   ├── _cards.scss     # Estilos de tarjetas
│   │   ├── _forms.scss     # Estilos de formularios
│   │   ├── _badges.scss    # Estilos de badges
│   │   ├── _lists.scss     # Estilos de listas
│   │   ├── _accordion.scss # Estilos de acordeón
│   │   ├── _modals.scss    # Estilos de modales
│   │   ├── _alerts.scss    # Estilos de alertas
│   │   ├── _progress.scss  # Barras de progreso
│   │   ├── _tabs.scss      # Tabs y pills
│   │   ├── _tooltips.scss  # Tooltips
│   │   ├── _dropdown.scss  # Dropdowns
│   │   └── _index.scss
│   ├── layout/
│   │   ├── _navbar.scss    # Navegación
│   │   ├── _footer.scss    # Footer
│   │   ├── _hero.scss      # Secciones hero
│   │   ├── _grid.scss      # Grid y flexbox custom
│   │   ├── _timeline.scss  # Timeline visual
│   │   └── _index.scss
│   ├── pages/
│   │   ├── _home.scss      # Estilos del home
│   │   ├── _about.scss     # Estilos sobre mí
│   │   ├── _projects.scss  # Estilos proyectos
│   │   ├── _blog.scss      # Estilos del blog
│   │   ├── _contact.scss   # Estilos contacto
│   │   └── _index.scss
│   └── main.scss           # Archivo principal
├── img/                    # Imágenes del proyecto
├── pages/
│   ├── blog.html          # Página del blog
│   ├── contacto.html      # Página de contacto
│   ├── proyectos.html     # Portfolio de proyectos
│   └── sobre-mi.html      # Información personal
├── index.html             # Página principal
├── package.json           # Configuración npm y scripts
├── .gitignore            # Archivos excluidos de Git
└── README.md             # Este archivo
```

## Instalación y Uso

### Requisitos previos
- Node.js instalado en tu sistema

### Instalación

1. Clona el repositorio:
```bash
git clone https://github.com/nandofag/blog-personal.git
cd blog-personal
```

2. Instala las dependencias:
```bash
npm install
```

### Comandos disponibles

```bash
# Compilar SASS una vez
npm run sass

# Compilar SASS en modo watch (desarrollo)
npm run sass:watch

# Compilar SASS comprimido (producción)
npm run build
```

### Ver el sitio

Abre `index.html` en tu navegador web preferido. No se requiere servidor local, todas las dependencias externas se cargan vía CDN.

## Páginas del Sitio

- **Home**: Página principal con presentación, proyectos destacados y últimas entradas del blog
- **Sobre Mí**: Información personal, educación, experiencia y habilidades
- **Proyectos**: Portfolio con proyectos realizados
- **Blog**: Artículos y tutoriales sobre desarrollo web
- **Contacto**: Formulario de contacto e información

## Características SASS Implementadas

### Variables (`_variables.scss`)
- Colores del tema (primarios, secundarios, estados)
- Tipografías
- Espaciados
- Border-radius
- Sombras
- Transiciones
- Breakpoints
- Mapas de valores para generación dinámica

### Mixins (`_mixins.scss`)
- `respond-to($breakpoint)` - Media queries mobile-first
- `respond-below($breakpoint)` - Media queries desktop-first
- `flex-center`, `flex-between`, `flex-column` - Utilidades flexbox
- `button-base`, `button-variant` - Estilos de botones
- `card-base`, `card-hover-effect` - Estilos de tarjetas
- `gradient-bg` - Gradientes
- `hover-underline`, `hover-lift` - Efectos hover
- `form-input-base` - Estilos de formularios
- Y muchos más...

### Funciones (`_functions.scss`)
- `get-color($name)` - Obtener color del mapa
- `shade($color, $percentage)` - Oscurecer color
- `tint($color, $percentage)` - Aclarar color
- `get-spacing($size)` - Obtener espaciado
- `px-to-rem($px)` - Conversión de unidades
- `grid-width($columns)` - Calcular ancho de columna

### Operadores y bucles
- `@each` para generar clases dinámicas de colores, espaciados, sombras
- `@for` para generar clases de gaps
- Operaciones matemáticas con `sass:math`
- Manipulación de colores con `sass:color`

### Nesting
Todo el código SCSS utiliza nesting para:
- Organizar selectores relacionados
- Usar `&` para modificadores y pseudo-elementos
- Crear estructura jerárquica clara

### @extend
Uso de `@extend` implícito a través de mixins que comparten estilos base.

## Uso de Flexbox y CSS Grid

### CSS Grid
- **Sección "Proyectos Destacados"** (`index.html`):
  - Clase `.proyectos-destacados-grid` usa `display: grid` con `grid-template-columns: repeat(auto-fit, minmax(300px, 1fr))`
  - Layout responsive que se adapta automáticamente

### Flexbox
- **Sección "Últimas Entradas del Blog"** (`index.html`):
  - Clase `.entradas-blog-flexbox` usa `display: flex` con `flex-wrap: wrap`
  - Las tarjetas usan `flex: 1 1 calc(33.333% - 2rem)`
- **Múltiples componentes**: cards, navbar, footer, timeline

## Compatibilidad

- Chrome (últimas versiones)
- Firefox (últimas versiones)
- Safari (últimas versiones)
- Edge (últimas versiones)

## Autor

Fernando Fagundez

## Licencia

Este proyecto es parte de un curso académico.

## Enlaces

- [Sitio en vivo](https://nandofag.github.io/blog-personal/)
- [Repositorio en GitHub](https://github.com/nandofag/blog-personal)
