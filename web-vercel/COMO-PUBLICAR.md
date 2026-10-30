# Cómo publicar la web de check-in de Rural Calaceite

Esta carpeta (`web-vercel`) ya está lista para subir. Contiene:
- `index.html` — página de inicio de la marca
- `casa-tomas.html` — guía de Casa Tomás (se verá en /casa-tomas)
- `casa-juliana.html` — guía de Casa Juliana (se verá en /casa-juliana)
- `vercel.json` — hace que las URLs salgan limpias (sin el `.html`)

---

## OPCIÓN A — Netlify Drop (la más fácil, sin saber nada técnico) ⭐ recomendada

1. Entra en **https://app.netlify.com/drop**
2. **Arrastra la carpeta `web-vercel` entera** a la zona que pone "Drag and drop".
3. En segundos te da una web online (ej. `algo-random.netlify.app`).
   - Tu inicio: `.../`
   - Casa Tomás: `.../casa-tomas`
   - Casa Juliana: `.../casa-juliana`
4. Crea una cuenta gratis cuando te lo pida (para que la web no caduque).

## OPCIÓN B — Vercel (necesita un paso más)

Vercel no deja arrastrar una carpeta sin más; pide conectarlo a GitHub o usar un comando.
La forma clicable:
1. Crea una cuenta gratis en **github.com**.
2. Crea un repositorio nuevo y sube los archivos de esta carpeta (botón "uploading an existing file").
3. En Vercel: **Add New ▸ Project ▸ Import** ese repositorio ▸ **Deploy**.

(Si te lías, usa la Opción A, que es inmediata.)

---

## Conectar tu dominio de IONOS

Una vez publicada (en Netlify o Vercel), para que salga en tu dominio:

### En Netlify
1. En tu web: **Domain settings ▸ Add a domain** y escribe tu dominio (ej. `checkin.tudominio.com`).
2. Netlify te dirá un valor **CNAME** (algo como `tu-sitio.netlify.app`).
3. Entra en **IONOS ▸ Dominios ▸ tu dominio ▸ DNS**.
4. Crea un registro **CNAME**:
   - Nombre/Host: `checkin` (o el subdominio que quieras)
   - Apunta a / Valor: lo que te dio Netlify
5. Guardar. Tarda de minutos a unas horas en activarse.

### En Vercel
1. En el proyecto: **Settings ▸ Domains ▸ Add** y escribe tu dominio.
2. Vercel te dará un **CNAME** (o una **A** si es dominio raíz).
3. En **IONOS ▸ DNS**, crea ese registro con el valor que te dé Vercel.
4. Guardar y esperar.

> Consejo: usa un **subdominio** tipo `checkin.tudominio.com` o `guia.tudominio.com`,
> así no tocas tu web principal si algún día tienes una.

---

## Cada mes (cambiar códigos/contraseñas)
Se edita el archivo de cada casa y se vuelve a subir (en Netlify, arrastras la carpeta otra vez; en Vercel, subes el cambio a GitHub). Laia + Claude lo pueden dejar hecho en un momento.
