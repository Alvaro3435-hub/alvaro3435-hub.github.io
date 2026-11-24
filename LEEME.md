# LaTeX editor: cómo obtener el APK

## 1. Publicar la carpeta (gratis, una sola vez)
1. Crea una cuenta en https://github.com y un repositorio nuevo, público, llamado `latex-editor`.
2. Pulsa **Add file → Upload files** y sube todos los archivos de esta carpeta (index.html, manifest.webmanifest, sw.js y los tres iconos). Pulsa **Commit changes**.
3. Entra en **Settings → Pages**. En *Branch* elige `main` y la carpeta `/ (root)`, y pulsa **Save**.
4. Espera 1 o 2 minutos. La app quedará en `https://TU_USUARIO.github.io/latex-editor/`.

## 2. Generar el APK
1. Abre https://www.pwabuilder.com y pega esa dirección.
2. Pulsa **Package for stores → Android → Generate package**.
3. Descarga el .zip. Dentro vienen:
   - un archivo **.apk**: el que se instala en la tablet;
   - un archivo .aab: solo sirve para Google Play;
   - la clave de firma (`signing.keystore` y `signing-key-info.txt`): guárdala, la necesitarás para actualizar la app;
   - `assetlinks.json`.

## 3. Quitar la barra del navegador (opcional, recomendado)
1. En el repositorio crea la carpeta `.well-known` y sube dentro `assetlinks.json`.
2. Crea también en la raíz un archivo vacío llamado `.nojekyll`; sin él GitHub no publica la carpeta `.well-known`.

## 4. Instalar en la tablet
1. Copia el .apk a la tablet y ábrelo.
2. Si Android lo pide, permite **Instalar apps de origen desconocido**.

## Notas
- La app funciona sin internet después de abrirla una vez.
- Tus proyectos se guardan dentro de la app. Usa **Guardar todo (.zip)** para tener respaldo.
- Sin instalar el APK, también puedes abrir la dirección en Chrome y elegir **⋮ → Instalar app**.
