# Lykos Method — Landing v2

Segunda versión del sitio de **Lykos Method** (Enzo Nievas), construida como evolución de la v1 (`../prototipo/`).

Mantiene el ADN de marca (paleta negro/oro, tipografías Fraunces + Hanken Grotesk + JetBrains Mono, columna 3D, bilingüe ES/EN, handoff a WhatsApp, deploy estático a GitHub Pages) y sube la vara en narrativa, evidencia e interactividad.

## Qué cambia respecto a v1

| Área | v1 | v2 |
|---|---|---|
| Hero | Logo 3D flotante | Split cinematográfico con retrato grande, callouts biomecánicos, badge "alumnos activos", scroll cue |
| Método | Grilla estática de 5 tarjetas | Scroll horizontal con snap, barra de progreso y controles |
| Proceso | Lista vertical de 5 pasos | Timeline interactivo: cliqueá un paso y se actualiza el panel lateral con imagen, descripción y checks |
| Anatomía | Columna 3D pasiva | Columna 3D con 4 hotspots clicables (cervical/torácica/lumbar/sacro) que enfocan y rotan el modelo |
| Entrenador | Bio estática + quote | Bio + creds + Q&A con chips directos a WhatsApp con mensaje pre-cargado |
| Alumnos | — | Sección nueva: KPIs animados (contadores), 3 testimonios, grilla de 6 placeholders de Instagram |
| Planes | 3 tarjetas verticales | 3 tarjetas + **toggle ARS/USD** + **tabla comparativa** completa |
| FAQ | — | Sección nueva: acordeón con 6 preguntas frecuentes |
| Contacto | Form + 2 canales | Form + 3 canales (WA, email, Instagram) |
| Micro-UX | Reveals, progress bar, dot nav | + Preloader, cursor custom, botones magnéticos, grain overlay, contadores animados, marquee de keywords |
| i18n | ES/EN con diccionario parcial | ES/EN con diccionario completo de todas las secciones nuevas |
| Performance | OK | `loading="lazy"` en todas las imágenes, `prefers-reduced-motion` respetado, fallback SVG de la columna |

## Cosas nuevas que vale la pena probar

1. **Hero** — hover sobre botones (magnetismo), scroll hacia abajo.
2. **Método** — arrastrar / botones prev/next / snap. Ver progreso de barra.
3. **Proceso** — hover / click en cada paso lateral — el panel derecho cambia imagen y detalle.
4. **Anatomía** — click en Cervical / Torácica / Lumbar / Sacro — la columna 3D se desplaza de zona.
5. **Planes** — tocá el toggle ARS / USD — los precios cambian en vivo. La tabla comparativa muestra qué incluye cada plan.
6. **FAQ** — acordeón con animación suave.
7. **Idioma** — switch ES/EN en el nav recorre todas las secciones (incluido el panel dinámico del proceso).
8. **Mobile** — todo responsive, el cursor custom se oculta en touch, el nav de puntos se oculta por debajo de 1000 px.

## Stack

- HTML + CSS + JS vanilla, single-file (mismo deploy que v1)
- **Three.js** (`esm.sh`) — columna 3D con hotspots
- **GSAP + ScrollTrigger** — rotación scroll-driven
- **Google Fonts** — Fraunces, Hanken Grotesk, JetBrains Mono
- **IntersectionObserver** — reveals y contadores
- **Unsplash** — placeholders de imagen hasta que Enzo mande fotos reales

## TODOs pendientes (datos del cliente)

- [ ] Reemplazar retrato SVG placeholder por foto real de Enzo (hero + sección Entrenador)
- [ ] Reemplazar placeholders de Instagram por capturas reales de `@lykosmethod`
- [ ] Validar precios finales (hoy: $55.000 / $120.000 / $200.000 en ARS)
- [ ] Validar testimonios (hoy hay 3 ficticios plausibles — confirmar con Enzo si usa reales)
- [ ] Confirmar WhatsApp `+54 9 261 625 7645`
- [ ] Registrar dominio y apuntar a GitHub Pages
- [ ] Agregar Google Analytics 4 y schema.org JSON-LD si se entrega en producción

## Deploy

Single-file HTML + logo.jpg. Apto para GitHub Pages, Netlify o cualquier hosting estático. Sugerencia: `github.com/jbarrancogit/lykos-method-v2` o deployar como branch paralela de `lykos-method`.

## Estructura

```
prototipo-v2/
├── index.html     # todo el sitio (single file, ~3500 líneas)
├── logo.jpg       # logo Lykos (copiado de v1)
└── README.md      # este archivo
```
