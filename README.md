# Mario Álvarez — Portfolio

Web personal (data science + deporte). Sitio estático de una sola página, sin build ni dependencias — HTML, CSS y JS puro. Bilingüe ES/EN con selector en la cabecera y en el footer.

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub (por ejemplo `mario-alvarez.github.io` para dominio raíz, o cualquier nombre para una project page).
2. Sube el contenido de esta carpeta (`index.html` + `assets/`) a la raíz del repo:
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

## Dominio propio (opcional)

Si quieres usar un dominio propio, añade un archivo `CNAME` en la raíz con el dominio (ej. `mario-alvarez.eu`) y configura los DNS de tu proveedor apuntando a GitHub Pages.

## Editar contenido

Todo el texto vive en `index.html`: el marcado usa atributos `data-i18n="clave"` y el objeto `translations` (al final del archivo, dentro de `<script>`) contiene las versiones ES y EN de cada clave. Para cambiar un texto, edítalo en ambos idiomas dentro de ese objeto.

Las imágenes y el CV están en `assets/`.
