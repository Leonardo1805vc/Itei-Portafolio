---
name: Leonardo Velazquez Corona — Portfolio
colors:
  night: "#070545"
  indigo: "#1C1A52"
  cream: "#F2E3C8"
  lavender: "#7772BE"
  white: "#FFFFFF"
  ink: "#17162B"
  primary: "{colors.night}"
  surface: "{colors.indigo}"
  accent: "{colors.cream}"
  interactive: "{colors.lavender}"
  text-on-dark: "{colors.white}"
  text-on-light: "{colors.ink}"
  # [REVISAR] Valores complementarios propuestos — no estaban en el doc original:
  overlay-dark: "rgba(7, 5, 69, 0.72)"
  shadow-low: "rgba(0, 0, 0, 0.18)"
  shadow-high: "rgba(0, 0, 0, 0.28)"
  disabled-bg: "rgba(119, 114, 190, 0.32)"
  disabled-text: "rgba(255, 255, 255, 0.48)"
  error: "#E5484D"
  success: "#30A46C"
typography:
  display:
    font: "Montserat"
    fallback: "'Arial Narrow', sans-serif"
    note: "[REVISAR] En el doc dice 'Montserat' — probable que sea 'Montserrat'. Confirmar familia y si es variante condensada."
    case: uppercase
    weight: 700
    size-min: 48px
    size-max: 96px
    line-height: 1.0
    letter-spacing: "0.01em"
    color: "{colors.cream}"
  subtitle:
    font: "{typography.display.font}"
    size-min: 22px
    size-max: 32px
    weight: 600
    line-height: 1.2
    color: "{colors.cream}"
  body:
    font: "Raleway"
    fallback: "system-ui, sans-serif"
    size: 17px
    size-min: 16px
    size-max: 18px
    weight: 400
    line-height: 1.6
    color-dark-bg: "{colors.white}"
    color-light-bg: "{colors.ink}"
  nav-button:
    font: "{typography.body.font}"
    size: 16px
    weight: 600
    line-height: 1.4
  caption:
    font: "{typography.body.font}"
    size: 14px
    line-height: 1.5
    # [REVISAR] Propuesto — no estaba en el original.
spacing:
  base: 4px
  scale: [4px, 8px, 12px, 16px, 24px, 32px, 48px, 64px, 96px, 128px]
  container-max: 1280px
  margin-mobile: 16px
  margin-tablet: 24px
  margin-desktop-min: 32px
  margin-desktop-max: 48px
  touch-min: 44px
  # [REVISAR] Breakpoints propuestos — no estaban en el original:
  breakpoint-tablet: 768px
  breakpoint-desktop: 1024px
rounded:
  button: 8px
  input: 8px
  project-card: 12px
  project-image: 12px
  info-card-min: 24px
  info-card-max: 28px
  pill: 999px
  # [REVISAR] Propuesto — no estaba en el original.
elevation:
  low: "0 6px 18px {colors.shadow-low}"
  high: "0 18px 48px {colors.shadow-high}"
  # [REVISAR] Sombras tomadas literales del doc; nombres de token propuestos.
motion:
  fast: 120ms
  base: 220ms
  section: 420ms
  easing: "cubic-bezier(0.2, 0, 0, 1)"
  lift: -2px
  control-shift-max: 8px
  texture-drift-max: 16px
  # [REVISAR] Easing propuesto — no estaba en el original.
components:
  button-primary:
    bg: "{colors.cream}"
    text: "{colors.night}"
    min-height: 48px
    padding: "12px 24px"
    radius: "{rounded.button}"
    font: "{typography.nav-button.font}"
    hover-bg: "{colors.white}"
    hover-lift: "{motion.lift}"
    focus-ring: "2px solid {colors.lavender}"
  button-secondary:
    bg: transparent
    border: "1px solid {colors.cream}"
    text: "{colors.cream}"
    min-height: 48px
    padding: "12px 24px"
    radius: "{rounded.button}"
    hover-bg: "{colors.white}"
    focus-ring: "2px solid {colors.lavender}"
  link:
    color: "{colors.lavender}"
    color-alt: "{colors.cream}"
    hover: underline
    focus-ring: "2px solid {colors.lavender}"
  nav:
    bg-top: transparent
    bg-scrolled: "{colors.night}"
    active-color: "{colors.cream}"
    active-marker: "línea o destello pequeño en {colors.cream}"
    mobile: "panel fullscreen, controles grandes, cierre visible"
  project-card:
    bg: "transparent o {colors.indigo} tenue"
    radius: "{rounded.project-card}"
    content: "imagen + categoría + nombre + descripción breve"
    hover-image: "scale ligero"
    hover-title-color: "{colors.cream}"
  input:
    min-height: 48px
    padding: "14px 16px"
    radius: "{rounded.input}"
    label: visible
    focus-border: "{colors.lavender}"
    error-style: "texto + icono, no solo color"
---

# Overview

Sistema de diseño de Leonardo Velázquez Corona para su portafolio personal.

Base editorial oscura en `{colors.primary}`, tipografía de gran escala en `{colors.accent}` y recursos gráficos en movimiento (trama de puntos, ondas, destello). La marca funciona como un escenario constante: el marco `{colors.night}` / `{colors.surface}` se mantiene, y cada proyecto aporta sus propios colores e imágenes dentro de su tarjeta o caso sin alterar los controles globales.

El sistema funciona cuando la identidad se reconoce entre proyectos distintos, la información se entiende con facilidad y cada recurso visual tiene una razón dentro de la composición.

# Colors

Paleta principal: azul marino, crema y gama de violetas. El contraste oscuro hace resaltar las imágenes; el crema aporta calidez.

- **Azul noche `{colors.night}`** — fondo principal y color que une todas las secciones. Usar como `nav.bg-scrolled`, fondo de página y marco general.
- **Índigo `{colors.indigo}`** — degradados, capas y fondos secundarios. Usar como `{colors.surface}` y fondo tenue de `project-card`.
- **Crema `{colors.cream}`** — títulos grandes, números y acentos editoriales. Usar en `{typography.display.color}`, `button-primary.bg` y `nav.active-color`.
- **Lavanda `{colors.interactive}`** — subtítulos, enlaces, foco y detalles interactivos. Usar en `{components.link.color}` y `{components.input.focus-border}`.
- **Blanco `{colors.white}`** — texto principal sobre fondos oscuros (`{colors.text-on-dark}`).
- **Tinta `{colors.ink}`** — lectura sobre fondos blancos o claros (`{colors.text-on-light}`).

> [REVISAR] Se agregaron tokens complementarios no definidos en el original: `{colors.overlay-dark}`, `{colors.disabled-bg}`, `{colors.disabled-text}`, `{colors.error}`, `{colors.success}`. Ajusta sus valores a tu gusto.

# Typography

Dos familias: condensada para titulares, sans limpia para lectura.

- **Display / Títulos:** `{typography.display.font}` en mayúsculas, `48–96px`, peso `700`, interlineado `1.0`. Color `{typography.display.color}`. Solo para aperturas, títulos de sección y números editoriales.
- **Subtítulos:** `{typography.display.font}`, `22–32px`. Identifican secciones secundarias.
- **Cuerpo:** `{typography.body.font}`, `17px` (nunca menos de `16px`, máximo `18px` en móvil), interlineado `1.6`. Color `{typography.body.color-dark-bg}` sobre `{colors.primary}` y `{typography.body.color-light-bg}` sobre claro.
- **Navegación y botones:** `{typography.nav-button.font}`, `16px`, peso `600`.

> [REVISAR] El doc dice "Montserat". Probablemente sea "Montserrat" (o "Montserrat Condensed"). Confirma familia exacta, pesos disponibles y si los titulares usan variante condensada real o solo mayúsculas con tracking.

# Layout

Retícula y espaciado editorial, composición asimétrica pero equilibrada.

- **Retícula:** 12 columnas en escritorio, 8 en tableta, 4 en móvil.
- **Contenedor:** máximo `{spacing.container-max}`, centrado.
- **Márgenes:** `{spacing.margin-mobile}` en móvil, `{spacing.margin-tablet}` en tableta, `{spacing.margin-desktop-min}–{spacing.margin-desktop-max}` en escritorio.
- **Escala de espacio:** `{spacing.scale}`. Valores pequeños (4–16px) organizan controles; valores grandes (48–128px) separan ideas y crean pausas entre proyectos.
- **Patrones de composición:**
  - Aperturas: título grande + imagen protagonista.
  - Casos de proyecto: pantalla dividida entre explicación y resultado visual.
  - Alternar texto e imagen para evitar recorridos repetitivos.
- **Reglas:** las imágenes pueden tocar el borde de la pantalla (full-bleed); los textos siempre conservan un ancho cómodo de lectura. Primero una pieza dominante, después detalles; evitar muchas miniaturas del mismo tamaño. Fotografías y mockups conservan su proporción.
- **Responsive:** diseños divididos → secuencia vertical (título → imagen principal → explicación). Galerías → secuencia vertical o carrusel accesible. Paneles que rodean un retrato → pasan debajo de la imagen. Títulos reducen tamaño pero conservan contraste display/cuerpo. Tramas se recortan a esquinas y bajan intensidad. Área táctil mínima `{spacing.touch-min}`; cuerpo `16–18px`.

> [REVISAR] Breakpoints `{spacing.breakpoint-tablet}` / `{spacing.breakpoint-desktop}` propuestos; define tus valores reales.

# Elevation & Depth

La profundidad se construye con superposición, escala y degradados en `{colors.indigo}`. Las tarjetas en reposo pueden mantenerse planas.

- **Elevación baja:** `{elevation.low}`.
- **Elevación alta:** `{elevation.high}`.
- Sombras suaves en negro; no usar sombras duras ni múltiples sombras apiladas.
- La imagen es la evidencia principal: contexto suficiente por caso (problema, concepto, solución) antes que decoración.

# Shapes

Composiciones basadas en rectángulos amplios y bloques editoriales.

- **Botones y campos:** `{rounded.button}`.
- **Tarjetas de proyecto e imágenes:** `{rounded.project-card}`.
- **Tarjetas de información:** `{rounded.info-card-min}–{rounded.info-card-max}`.
- **Recursos de firma:** trama de puntos, ondas y destello. Usar en esquinas, transiciones o pausas visuales; nunca detrás de textos largos ni encima de elementos importantes; nunca todos a la vez en la misma pantalla.

# Components

Todos los componentes contemplan estados reposo, hover, foco, presión, deshabilitado y carga cuando aplique. Foco siempre visible con `{colors.interactive}`. Movimiento: rápido `{motion.fast}`, estados `{motion.base}`, secciones `{motion.section}`, easing `{motion.easing}`. Respetar `prefers-reduced-motion` (eliminar escalas y desplazamientos; conservar cambios de color o borde).

## Navegación

Simple, con accesos a proyectos, perfil y contacto. Sobre portada puede ser transparente (`{components.nav.bg-top}`); al desplazar usa `{components.nav.bg-scrolled}`. Enlace activo en `{components.nav.active-color}` con línea o destello pequeño. En móvil: `{components.nav.mobile}`.

## Botones y enlaces

- **Primario (`{components.button-primary.bg}` / `{components.button-primary.text}`):** altura mínima `48px`, padding `{components.button-primary.padding}`, radio `{rounded.button}`. En hover cambia a `{components.button-primary.hover-bg}` y sube `{motion.lift}` con transición `{motion.base}`.
- **Secundario:** transparente con borde y texto `{colors.cream}`; mismo tamaño y radio que el primario.
- **Enlaces de texto:** `{components.link.color}` o `{components.link.color-alt}`, subrayado al hover.

## Tarjetas y proyectos

`{components.project-card.bg}`, radio `{rounded.project-card}`. Contenido: imagen + categoría + nombre + descripción breve. Hover: imagen con aumento ligero + título en `{components.project-card.hover-title-color}`. Los colores propios de cada proyecto viven dentro de su tarjeta o caso y no cambian los controles globales.

## Formularios y estados

Etiqueta visible, altura mínima `48px`, relleno `14×16px`, radio `{rounded.input}`. Foco en `{components.input.focus-border}`. Errores con `{components.input.error-style}` (usar `{colors.error}`). Controles con desplazamiento máximo `{motion.control-shift-max}`; texturas de fondo con deriva lenta hasta `{motion.texture-drift-max}`.

> [REVISAR] Estilos de `disabled`, `pressed` y `loading`, así como el icono de error y el color `{colors.error}` / `{colors.success}`, propuestos por completitud. Define tus valores finales.

# Do's and Don'ts

## Lo que mantengo (Do's)

- El azul noche `{colors.primary}` como marco principal de identidad.
- Títulos crema `{colors.accent}` de gran escala para abrir y separar secciones.
- Jerarquía clara: título → explicación → imagen.
- Libertad cromática de cada proyecto dentro de un espacio controlado (su tarjeta/caso).
- Recursos gráficos (puntos, ondas, destello) solo cuando dirigen, separan o dan ritmo.
- Explicación de problema, concepto y solución en cada caso.

## Lo que evito (Don'ts)

- Usar todas las tramas, ondas y destellos en una misma pantalla.
- Colocar texturas detrás de párrafos o información crítica.
- Usar tipografía condensada `{typography.display.font}` en textos largos o controles pequeños — ahí va `{typography.body.font}`.
- Agregar un color global nuevo por cada proyecto.
- Mostrar solo mockups sin explicar el propósito del trabajo.
- Afirmar resultados no comprobados.
