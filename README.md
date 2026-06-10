# carlosiwi.com — redesign

Rediseño del portfolio de Carlos Iwi, enfocado a la búsqueda de empleo como
**Senior Product Designer**.

## Estructura

- `index.html` — página principal (one-page)
- `styles.css` — estilos (light/dark, responsive, sin frameworks)
- `script.js` — toggle de tema, menú móvil, animaciones de scroll

## Decisiones de diseño

- **Enfocado a recruiters**: badge "Open to new opportunities", CTAs claros
  (email + descarga de CV), stats rápidas en el hero, sección "How I work"
  y timeline de experiencia.
- **Contenido en inglés** para maximizar el alcance en procesos de selección
  internacionales/remote.
- **Sin dependencias**: HTML/CSS/JS estático, desplegable en cualquier hosting
  (GitHub Pages, Netlify, el hosting actual…). Solo carga Google Fonts.
- Los enlaces a los case studies apuntan a las páginas existentes del dominio
  (`genially-connectors.html`, `genially-favorites.html`, `gh-dashboard.html`)
  y al PDF del CV (`Carlos_Iwi-Resume--lite_version.pdf`).

## Pendiente de completar (TODO)

- [ ] Fechas reales en la sección **Experience** (los `timeline-period` están
      vacíos salvo el puesto actual).
- [ ] Confirmar la URL exacta de LinkedIn.
- [ ] Sustituir los bloques de color de los case studies por capturas reales
      de cada proyecto.
- [ ] Revisar/ajustar el copy del hero y el "About" al tono personal de Carlos.
