# Blog — diezvariante.cl/blog

Blog personal hecho con [Quarto](https://quarto.org). Publicado en https://diezvariante.cl/blog.

## Crear un post nuevo

1. Crea una carpeta dentro de `posts/` con el nombre del post (en kebab-case, sin acentos):

   ```
   posts/
   └── mi-post-nuevo/
       └── index.qmd
   ```

2. En `index.qmd` pon esta cabecera y escribe abajo en Markdown:

   ```yaml
   ---
   title: "Título del post"
   description: "Una oración corta que describe el contenido."
   date: "2026-05-08"
   categories: [Transporte]
   ---

   El contenido del post va aquí, en Markdown normal.
   ```

   Categorías disponibles: `Transporte`, `Eléctrica`, `Música`, `Fotos`, `Otros`. Puedes poner varias: `categories: [Música, Otros]`.

3. Publica:

   ```bash
   git add .
   git commit -m "Nuevo post: título"
   git push
   quarto publish gh-pages --no-prompt --no-browser
   ```

## Agregar una imagen a un post

Las imágenes se guardan en el repo `Pablolog42.github.io` (clonado en `C:\Users\Pablo\Desktop\Pablolog42.github.io`), dentro de `assets/img/`.

1. Copia tu imagen a `Pablolog42.github.io/assets/img/`:

   ```bash
   cp "ruta/a/foto.jpg" "C:\Users\Pablo\Desktop\Pablolog42.github.io\assets\img\"
   ```

2. Súbela a GitHub:

   ```bash
   cd "C:\Users\Pablo\Desktop\Pablolog42.github.io"
   git add assets/img/foto.jpg
   git commit -m "Add foto.jpg"
   git push
   ```

3. Referénciala en cualquier post con la URL absoluta:

   ```markdown
   ![Descripción de la foto](https://diezvariante.cl/assets/img/foto.jpg)
   ```

Para PDFs y otros documentos: misma idea pero en `assets/docs/`, y referencia con `https://diezvariante.cl/assets/docs/archivo.pdf`.

## Previsualizar localmente

```bash
quarto preview
```

Abre `http://localhost:4321` con recarga automática al guardar.
