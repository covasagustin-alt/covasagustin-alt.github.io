# Landing — Reparaciones PC Box

Landing de una sola página para vender el software de gestión de reparaciones.

## Cómo verla en local

Abre `index.html` directamente con doble click — se abre en tu navegador. No necesita servidor.

Si prefieres servir vía HTTP (recomendado para probar todo correctamente):
```bash
cd C:\proyectos\landing-reparaciones
python -m http.server 8080
```
Luego abres http://localhost:8080.

## Qué editar antes de publicar

Busca y reemplaza estos placeholders en `index.html`:

| Placeholder | Significa |
|---|---|
| `[NOMBRE_DE_TU_EMPRESA]` | Tu nombre o el de la empresa (footer copyright). |
| `[EMAIL_CONTACTO]` | Email donde llegan los contactos (en el bloque CTA). |
| `[PRECIO_1]` | Precio del tier "Tienda única". |
| `[PRECIO_2]` | Precio del tier "Cadena de tiendas". |

Otras cosas que probablemente quieras tocar:

- **Capturas reales**: en la sección `#capturas` hay 4 placeholders gris-azulado. Sustituye cada `<div class="screenshot-placeholder">…</div>` por `<img src="capturas/nombre.png" alt="..." />` con tus capturas reales. Crea una carpeta `capturas/` al lado de `index.html`.
- **Mockup del hero**: el bloque con la cara fake del listado lo puedes dejar (queda bien estilizado) o sustituir por una captura real de la app.
- **Formulario de contacto**: actualmente solo muestra un alert con los datos. Conéctalo a un servicio real:
  - **Formspree** (gratis hasta 50 envíos/mes): cambia el `<form>` para que envíe a su endpoint.
  - **Tally / Typeform**: embeber el formulario externo.
  - **Tu propio backend**: si quieres recibir los datos en una BD propia.
- **Funcionalidades** (`#funcionalidades`): edita textos si quieres distinto tono o quitas/añades cards.
- **Pricing**: ajusta tiers y bullets a tu modelo real.

## Cómo publicarla

Es HTML/CSS estático puro — funciona en cualquier hosting:

### Opción 1 · GitHub Pages (gratis)
1. Sube esta carpeta a un repo público de GitHub.
2. Settings → Pages → Source → main branch → root.
3. En 2 minutos tienes `https://tuusuario.github.io/landing-reparaciones`.

### Opción 2 · Vercel / Netlify (gratis, profesional)
- Arrastra la carpeta a https://vercel.com o https://netlify.com.
- Despliegue en segundos. Permite conectar tu dominio propio.

### Opción 3 · Tu propio hosting
- Sube `index.html` y `styles.css` por FTP a tu hosting. Listo.

## Tono y diseño

- **Estilo SaaS moderno**: paleta azul/púrpura con gradientes sutiles, mucho espacio en blanco, tipografía sin remates.
- **Responsive**: se adapta a móvil (las tarjetas se apilan, los menús se simplifican).
- **Sin dependencias externas**: sin librerías, sin Bootstrap, sin Tailwind. Solo HTML + CSS vanilla. Carga rápido y se mantiene fácil.
- **Sin JavaScript** (salvo el alert demo del formulario, que sustituirás por el servicio real).
