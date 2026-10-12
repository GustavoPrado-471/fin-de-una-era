# El fin de una era 🪟

Landing estática de nuestra historia, con carrusel de 52 recuerdos, textos publicados, fotos, videos y nieve animada en la sección final. Diseño adaptable a móviles.

## Ejecutar en tu equipo

Requiere Python 3, sin instalar dependencias ni compilar:

```bash
python3 -m http.server 8000 --directory dist
```

Abre http://localhost:8000 en el navegador. Detén el servidor con Ctrl+C.

## Archivos

- `dist/index.html`: estructura y textos de las secciones.
- `dist/style.css`: estilos, diseño responsive y carrusel.
- `dist/snow.css`: animación de nieve y fondos de invierno.
- `dist/app.js`: carrusel, textos de recuerdos, editor y animaciones.
- `dist/assets/`: imágenes y videos utilizados por la página, además de recursos conservados de versiones anteriores.

Los textos compartidos están incluidos en `publishedWords` dentro de `dist/app.js`. Las claves son los números originales de las fotos, incluidos números decimales; no son la posición actual del carrusel. No cambies las claves al editar los textos. Conserva emojis y saltos de línea como cadenas JavaScript válidas.

Si actualizas `publishedWords`, cambia también `publishedRevision` a un valor nuevo para aplicar esa publicación a navegadores que ya habían visitado la página. Los cambios hechos desde el editor de la página se guardan solo en el navegador: exportarlos no modifica el repositorio ni publica una nueva versión.

## Subir a un repositorio

Descomprime el ZIP y abre una terminal dentro de esta carpeta:

```bash
git init
git add .
git commit -m "Landing El fin de una era"
git branch -M main
```

Crea un repositorio vacío en tu proveedor Git, copia su URL y ejecuta (sustituye `URL_DE_TU_REPOSITORIO`):

```bash
git remote add origin URL_DE_TU_REPOSITORIO
git push -u origin main
```

## Despliegue independiente

Publica el contenido de `dist/` en un hosting estático. No requiere comando de build, servidor de aplicación, base de datos ni variables de entorno. La carpeta pública debe ser `dist`; su `index.html` es la entrada.

Las imágenes, los videos y los textos se incluyen en el paquete. Las fuentes tipográficas se cargan desde Google Fonts y tienen fuentes de respaldo si no hay conexión. Los controles de edición usan almacenamiento local del navegador.

## Versión exportada

Página: https://el-fin-de-una-era.roundmoon9.chatgpt.site

Commit de origen: `07b4de97c29034fae5796a5428b7d2a95bd2cc3f`.

Exportación del 12 de octubre de 2026, después de mover la nieve al final y eliminar la foto original 30. Este paquete es independiente y no incluye credenciales, historial Git ni configuración interna del hosting original. No incluye una licencia que conceda derechos sobre las fotos personales.
