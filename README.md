# favoritul.github.io

Landing personal — Full Stack Engineer. Single-file HTML, sin dependencias de build.

## Desplegar en GitHub Pages (5 minutos)

1. **Crea un repositorio público** en tu cuenta `favoritul` con el nombre exacto:
   `favoritul.github.io`
   (debe coincidir con tu username de GitHub para que se publique en la raíz del dominio).

2. **Sube los archivos** de esta carpeta al repo (`index.html`, `.nojekyll`, este `README.md`).
   Desde la terminal:
   ```bash
   cd "C:\Users\favor\Documents\ClaudeCodeProjects\trabajo"
   git init
   git add index.html .nojekyll README.md
   git commit -m "Initial commit: landing personal estilo Linear"
   git branch -M main
   git remote add origin https://github.com/favoritul/favoritul.github.io.git
   git push -u origin main
   ```

3. **Activa GitHub Pages**: en el repo → Settings → Pages → Source: `Deploy from branch` → Branch: `main` / `(root)` → Save.

4. **Espera 30–60 segundos**. Tu sitio estará en:
   👉 `https://favoritul.github.io`

## Archivos

| Archivo      | Para qué sirve |
|--------------|---------------|
| `index.html` | La landing completa. Todo va aquí: HTML + CSS + JS embebidos. |
| `.nojekyll`  | Evita que GitHub procese el sitio como Jekyll (deja servir el HTML tal cual). |
| `README.md`  | Este archivo. No se publica como página. |

## Personalizar

- **Texto**: edita `index.html` directamente. Las secciones están comentadas (`<!-- ============== HERO ============== -->`).
- **Color de acento**: en el bloque `:root` al inicio del `<style>`, cambia `--accent` (#5e6ad2) y `--grad`.
- **Métricas**: bloque `<section class="metrics">` — los tres `.kpi` son las cifras destacadas.
- **Foto**: si quieres reemplazar las iniciales del avatar por una foto, sustituye el `<div class="avatar">A</div>` (sección `about-card`) por una `<img>`.

## Dominio propio (opcional)

Si en el futuro compras un dominio (por ejemplo `alinmoraru.dev`):
1. Crea un archivo `CNAME` en la raíz con el dominio (sin `https://`).
2. En tu DNS, apunta el dominio a `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` (registros A) o configura un CNAME a `favoritul.github.io`.
3. Settings → Pages → Custom domain → guardar.

## Soporte navegadores

Chrome / Edge / Safari / Firefox versiones actuales (2024+). Usa `backdrop-filter`, CSS variables, IntersectionObserver y `prefers-reduced-motion`. Mobile-first responsive.
