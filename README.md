# Mario Álvarez — Portfolio

Web personal (data science + deporte). Sitio estático de una sola página, sin build ni dependencias — HTML, CSS y JS puro. Bilingüe ES/EN con selector en la cabecera y en el footer.

## Estructura del proyecto

```
mario-alvarez-web/
├── index.html              # La web completa (HTML + CSS + JS en un archivo)
├── site.webmanifest        # Manifest PWA (nombre, colores, iconos de app)
├── robots.txt              # Indexación para buscadores
├── sitemap.xml             # Mapa del sitio
├── .nojekyll               # Evita que GitHub Pages procese la carpeta
├── .gitattributes          # Normalización de saltos de línea
├── .gitignore              # Archivos que Git debe ignorar
├── README.md               # Este archivo
└── assets/
    ├── img/                # Imágenes de contenido
    │   └── mario.jpg       # Foto de perfil
    ├── logo/               # Logotipo en distintos formatos
    │   ├── logo.png
    │   ├── logo.jpg
    │   └── mark.png        # Solo el símbolo (isotipo)
    ├── icons/              # Favicons e iconos de app / PWA
    │   ├── favicon-32.png
    │   ├── favicon-48.png
    │   ├── apple-touch-icon.png
    │   ├── icon-192.png
    │   ├── icon-512.png
    │   └── icon-master.png
    └── docs/               # Documentos descargables
        └── CV_Mario_Alvarez.pdf
```

> Todas las rutas del `index.html` ya apuntan a estas subcarpetas. Si mueves un
> archivo, actualiza su referencia en `index.html`.

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub (por ejemplo `mario-alvarez.github.io` para dominio raíz, o cualquier nombre para una project page).
2. Sube el contenido de esta carpeta (con su estructura) a la raíz del repo:
   ```
   git init
   git add .
   git commit -m "Primer despliegue"
   git branch -M main
   git remote add origin https://github.com/<tu-usuario>/<tu-repo>.git
   git push -u origin main
   ```
3. En GitHub → **Settings → Pages**, selecciona la rama `main` y la carpeta `/ (root)`.
4. La web quedará publicada en `https://<tu-usuario>.github.io/<tu-repo>/` (o en tu dominio raíz si el repo se llama `<tu-usuario>.github.io`).

El archivo `.nojekyll` ya está incluido para que GitHub Pages sirva la carpeta tal cual, sin procesarla.

## Publicar con Netlify (alternativa, sin Git)

Entra en [netlify.com/drop](https://app.netlify.com/drop) y arrastra esta carpeta entera. En segundos tendrás una URL pública.

## Dominio propio (opcional)

1. Añade un archivo `CNAME` en la raíz con tu dominio (ej. `mario-alvarez.eu`).
2. Configura los DNS de tu proveedor apuntando a GitHub Pages / Netlify.
3. Sustituye `TU-DOMINIO` en `robots.txt` y `sitemap.xml` por tu dominio real.

## Editar contenido

Todo el texto vive en `index.html`: el marcado usa atributos `data-i18n="clave"` y el objeto `translations` (al final del archivo, dentro de `<script>`) contiene las versiones ES y EN de cada clave. Para cambiar un texto, edítalo en **ambos idiomas** dentro de ese objeto.

Las imágenes están en `assets/img/` y `assets/logo/`, los iconos en `assets/icons/` y el CV en `assets/docs/`.
