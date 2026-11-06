# favoritul.github.io

Portfolio personal de **Alin-Valentin Moraru** — desarrollador Full Stack (Java / Spring Boot / .NET).

En producción: **https://favoritul.github.io**

Un solo fichero HTML, sin build, sin dependencias de npm. HTML + CSS + JS embebidos en `index.html`.

## Estructura del sitio

| Sección | Ancla | Contenido |
|---|---|---|
| Hero | — | Presentación, CTAs y descarga del CV |
| Métricas | `#metrics` | Tres cifras destacadas de la trayectoria |
| Proyectos | `#projects` | Sistema de facturación en Java y en .NET |
| Experiencia | `#experience` | Timeline profesional |
| Stack | `#stack` | Tecnologías agrupadas por área |
| Enfoque | `#about` | Cómo trabajo |
| Contacto | `#contact` | Email, LinkedIn y GitHub |

## Proyectos enlazados

- [sistema-facturacion-java](https://github.com/favoritul/sistema-facturacion-java) — Java 25, Spring Boot 4, Spring Cloud Gateway, MySQL, Docker
- [sistema-facturacion-net](https://github.com/favoritul/sistema-facturacion-net) — .NET 10, ASP.NET Core, EF Core, YARP, MySQL, Docker

El mismo dominio resuelto en los dos ecosistemas, para separar lo que es decisión de arquitectura de lo que es sintaxis del framework.

## Ficheros

| Fichero | Para qué sirve |
|---|---|
| `index.html` | El sitio completo. Todo va aquí. |
| `cv-alin-valentin-moraru.pdf` | CV enlazado desde el botón "Descargar CV" del hero. |
| `.nojekyll` | Evita que GitHub Pages procese el sitio como Jekyll. |
| `README.md` | Este fichero. No se publica. |

## Cómo editar

```bash
cd "C:\Users\favor\Documents\ClaudeCodeProjects\trabajo"
# editar index.html
git add -A
git commit -m "Describe el cambio"
git push
```

GitHub Pages republica solo, en 30–60 segundos. Si no ves el cambio, recarga con `Ctrl+F5` (caché del navegador).

### Dónde tocar cada cosa

- **Texto**: las secciones están comentadas en `index.html` (`<!-- ============== HERO ============== -->`).
- **Color de acento**: bloque `:root` al inicio del `<style>` — `--accent` (`#5e6ad2`) y `--grad`.
- **Añadir un proyecto**: duplica un `<article class="proj">` dentro de `.proj-grid`.
- **Animación de entrada**: las clases `.reveal` las activa un `IntersectionObserver` al hacer scroll. Un elemento nuevo sin `.reveal` sale visible desde el principio.

## Actualizar el CV

Sustituye `cv-alin-valentin-moraru.pdf` manteniendo el mismo nombre de fichero y haz commit. El enlace del hero no cambia.

## Dominio propio (opcional)

1. Crea un fichero `CNAME` en la raíz con el dominio, sin `https://`.
2. En el DNS, registros A a `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, o un CNAME a `favoritul.github.io`.
3. Settings → Pages → Custom domain → guardar.

## Navegadores

Chrome / Edge / Safari / Firefox actuales. Usa `backdrop-filter`, variables CSS, `IntersectionObserver` y `prefers-reduced-motion`. Responsive mobile-first.
