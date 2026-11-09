# Álbum de fotos de la boda · Cecilia & Eduardo

Página web para que los invitados suban sus fotos desde el celular y todos las vean **en vivo**.
Las fotos se guardan en la carpeta de **Google Drive** de los novios. Los invitados **no necesitan cuenta**.

Incluye:
- Subir fotos desde la **galería** o la **cámara** (varias a la vez).
- **Momento** de cada foto (Iglesia, Fiesta, Vals, Mesa dulce) y **filtros** en la galería.
- **Retos fotográficos** con tabla de posiciones.
- **Se instala como app** en la pantalla de inicio, con el ícono C&E.
- **Modo pantalla** para el proyector del salón (`?pantalla`).

## Archivos

| Archivo | Va en |
|---|---|
| `index.html` | GitHub |
| `manifest.webmanifest` | GitHub |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png`, `favicon.png` | GitHub |
| `Code.gs` | Google Apps Script (no va en GitHub) |
| `README.md` | Esta guía (opcional en GitHub) |

---

## 1. Actualizar el script de Google (obligatorio con esta versión)
1. Abrí tu proyecto en [script.google.com](https://script.google.com).
2. Borrá todo el código y pegá el nuevo `Code.gs` (ya tiene el ID de la carpeta). Guardá 💾.
3. **Implementar → Administrar implementaciones → ✏️ (lápiz)** → en *Versión* elegí **Nueva versión** → **Implementar**.
   Así la dirección `/exec` sigue siendo la misma y no hay que tocar `index.html`.

> Si no hacés el paso 3, las fotos se van a subir igual pero **sin reto ni momento**.

## 2. Subir los archivos a GitHub
1. Entrá a tu repositorio → **Add file → Upload files**.
2. Arrastrá **todos** los archivos de la tabla de arriba que van en GitHub (podés soltar todos juntos).
3. **Commit changes**. En 1 o 2 minutos se actualiza la página.

## 3. Probar
- Abrí la página en el celular, poné tu nombre, elegí un momento y un reto, y subí una foto.
- Tiene que aparecer en la galería con la etiqueta ★ del reto, en la tabla de posiciones y en la carpeta de Drive.
- Probá los filtros (Iglesia, Fiesta, etc.) y el aviso “Tené el álbum como app”.

---

## Cómo instalarla como app (para contarles a los invitados)
- **Android (Chrome):** aparece el botón **Instalar** en el aviso, o menú ⋮ → *Agregar a pantalla principal*.
- **iPhone (Safari):** botón **Compartir** (cuadrado con flecha) → *Agregar a inicio*.
Queda un ícono “Ceci & Edu” en la pantalla de inicio que abre el álbum como una app.

## El día de la boda
- **QR en las mesas** con la dirección de la página.
- **Modo pantalla:** en la compu del proyector abrí `https://TU-USUARIO.github.io/fotos-boda/?pantalla`
  y hacé clic una vez para pantalla completa. Las fotos nuevas aparecen enseguida, con el nombre y el reto.
- **Borrar una foto:** borrala de la carpeta de Drive; en segundos desaparece de la página.
- **Ganador de los retos:** el primero de la *Tabla de posiciones* (cuenta retos distintos; si hay empate, gana quien llegó primero).
  Revisen las fotos antes de dar el premio, por si alguien marcó un reto que no cumplió 😉.

## Personalizar (en `index.html`, al principio del `<script>`)
- `RETOS`: la lista de retos. Agregá, sacá o cambiá el texto.
  ⚠️ Una vez que empiecen a subir fotos **no cambies el texto** de un reto: las fotos viejas quedarían con el nombre anterior.
- `MOMENTOS`: los momentos/filtros.
- `CADA_CUANTO`, `SEG_PANTALLA`, `LADO_MAX`: tiempos y tamaño de las fotos.

## Para tener en cuenta
- Las fotos se achican a 1920 px (~0,5 MB) para que suban rápido con poca señal.
- Solo fotos, no videos.
- Cualquiera con el link puede ver y subir: compártanlo con los invitados, no en redes.
- Las fotos del Paso 1 anterior (sin reto ni momento) siguen apareciendo en “Todas”.
