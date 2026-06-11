# Contribuir a WebForge

¡Gracias por tu interés en contribuir! WebForge es un proyecto open source y toda ayuda es bienvenida, ya sea corrigiendo errores, mejorando contenido, agregando secciones o mejorando el código.

## Tabla de contenidos

- [Código de conducta](#código-de-conducta)
- [Cómo contribuir](#cómo-contribuir)
- [Reportar bugs](#reportar-bugs)
- [Solicitar funcionalidades](#solicitar-funcionalidades)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Convenciones](#convenciones)
- [Proceso de Pull Request](#proceso-de-pull-request)

## Código de conducta

Sé respetuoso con otros contribuyentes. No se toleran insultos, discriminación ni conductas agresivas. Usamos este espacio para aprender y compartir conocimiento, así que mantengamos un ambiente amable y constructivo.

## Cómo contribuir

### Áreas donde podés ayudar

- **Corregir typos o errores de ortografía** en cualquier archivo HTML o Markdown.
- **Mejorar explicaciones** — si algo no está claro o le falta profundidad.
- **Reportar errores** — links rotos, contenido desactualizado, bugs visuales.
- **Agregar contenido** — nuevas secciones, ejemplos, cheatsheets.
- **Mejorar la accesibilidad** — atributos ARIA, contraste, navegación por teclado.
- **Optimizar performance** — cargar menos recursos, mejorar tiempos de respuesta.

### Pasos básicos

1. **Fork** el repositorio desde GitHub.
2. **Cloná** tu fork localmente:
   ```bash
   git clone https://github.com/TU_USUARIO/WebForge.git
   cd WebForge
   ```
3. **Creá una rama** para tu cambio:
   ```bash
   git checkout -b fix/corregir-typos-seccion-css
   ```
4. **Hacé tus cambios** y verificá que todo funcione correctamente.
5. **Commiteá** con un mensaje descriptivo (ver [Convenciones de commits](#convenciones-de-commits)).
6. **Subí** tu rama al fork:
   ```bash
   git push origin fix/corregir-typos-seccion-css
   ```
7. **Abrí un Pull Request** contra la rama `main` del repo original.

## Reportar bugs

Si encontrás un problema, abrí un issue con la siguiente información:

- **Descripción** del problema.
- **Pasos para reproducirlo** (qué hiciste, qué esperabas, qué pasó).
- **Captura de pantalla** si es un problema visual.
- **Navegador y versión** donde lo encontraste.
- **Dispositivo** (desktop, mobile, tablet).

## Solicitar funcionalidades

¿Te falta algo en WebForge? Abrí un issue con el tag `enhancement` describiendo:

- Qué te gustaría que exista.
- Por qué lo considerás útil para otros usuarios.
- Si tenés alguna referencia o ejemplo de cómo debería verse.

## Estructura del proyecto

```
├── index.html              # Landing page
├── 404.html                # Página de error
├── sections/               # Páginas de contenido por tema
├── cheatsheets/            # Cheatsheets de referencia rápida
├── components/             # HTML compartidos (header, sidebar, footer)
├── css/
│   ├── variables.css       # Custom properties (colores, fuentes, espaciado)
│   ├── layout.css          # Estructura general, grid layout
│   ├── components.css      # Componentes reutilizables (cards, tablas, botones)
│   └── print.css           # Estilos de impresión
├── js/
│   ├── app.js              # Punto de entrada, orquesta la carga de componentes
│   ├── common-loader.js    # Fetch de header/sidebar/footer
│   ├── sidebar.js          # Toggle y navegación del sidebar
│   ├── search.js           # Buscador con índice JSON
│   ├── code-blocks.js      # Botón copiar y syntax highlighting
│   └── scroll-animations.js# Animaciones al hacer scroll
├── data/
│   └── search-index.json   # Índice de búsqueda para el buscador
└── assets/                 # Imágenes y fuentes
```

## Convenciones

### Convenciones de commits

Usá [Conventional Commits](https://www.conventionalcommits.org/) para los mensajes:

| Prefijo | Uso |
|---------|-----|
| `feat:` | Nueva funcionalidad o contenido |
| `fix:` | Corrección de un bug |
| `docs:` | Cambios en documentación (README, PRD, CONTRIBUTING) |
| `style:` | Cambios de formato (indentación, espacios, sin lógica) |
| `refactor:` | Refactor de código sin cambio funcional |
| `a11y:` | Mejoras de accesibilidad |
| `perf:` | Mejoras de performance |

Ejemplos:
```
feat: agregar sección de CSS Grid
fix: corregir link roto en cheatsheet de Git
docs: actualizar README con nuevas badges
a11y: agregar aria-label a botones del sidebar
```

### Convenciones de contenido

- **Idioma**: todo el contenido está en **español rioplatense** (voseo: "tenés", "podés", "creá", "funcioná").
- **Tono**: informal pero claro, como un compañero que te explica.
- **Código**: los ejemplos de código van en inglés (nombres de variables, funciones, comentarios dentro del código).
- **HTML**: usá etiquetas semánticas (`<section>`, `<article>`, `<nav>`, `<main>`).
- **CSS**: usá las custom properties definidas en `variables.css`, evitá colores hardcodeados.
- **Nuevas secciones**: seguí la estructura de las secciones existentes (breadcrumb, navegación prev/next, sub-secciones con `<h2>` y `<h3>`).

### Convenciones de accesibilidad

- Todo ícono decorativo lleva `aria-hidden="true"`.
- Los botones sin texto visible llevan `aria-label` descriptivo.
- Las imágenes llevan `alt` descriptivo (o `alt=""` si son decorativas).
- Los formularios tienen `<label>` asociados.
- El contraste de texto cumple WCAG AA (mínimo 4.5:1 para texto normal).

## Proceso de Pull Request

1. Asegurate de que tu rama esté actualizada con `main`.
2. Verificá que el sitio funcione correctamente abriendo los archivos en un navegador local.
3. Si cambiaste contenido, revisá que no haya typos y que el voseo sea consistente.
4. Si agregaste una sección nueva, actualizá el sidebar (`components/sidebar.html`) y el índice de búsqueda (`data/search-index.json`).
5. Escribí una descripción clara del PR explicando qué cambia y por qué.
6. Respondé a los comentarios del review de forma constructiva.

---

¿Dudas? Abrí un issue y preguntá tranquilamente. No hay preguntas tontas.