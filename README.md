# Avance del año

Una página web simple que muestra qué porcentaje del año transcurrió, con un canvas encima donde podés agregar tus propias notas, imágenes, eventos y checklists.

## ¿Para qué?

En muchos lugares de trabajo se dibuja a mano en un pizarrón una barra que indica cuánto del año ya pasó, y la cuenta se hace manualmente cada vez. Esta página automatiza esa tarea, y además funciona como un pizarrón digital liviano para anotar lo que quieras al lado de la barra.

## Qué muestra

### Avance del año
- Porcentaje del año con dos decimales
- Barra de progreso visual
- Días transcurridos y días restantes
- Fecha actual en español

Se actualiza solo cada minuto.

### Canvas (pizarrón)

Sobre la página podés agregar y arrastrar libremente:

- **📷 Imágenes** — desde el botón o pegando con `Ctrl+V`
- **T Texto** — editable con doble clic, con color y tamaño ajustables
- **📅 Eventos** — cuenta regresiva (o tiempo transcurrido) hacia una fecha
- **✅ Checklists** — listas de tareas marcables

Todos los elementos se pueden mover, redimensionar y borrar. Se guardan automáticamente en el navegador (localStorage), así que siguen ahí cuando volvés a abrir la página.

### Modo oscuro

Botón 🌙 para alternar entre claro y oscuro. La preferencia se recuerda.

### Compartir

El botón 📤 genera un link que incluye los textos, eventos y checklists del canvas codificados en la URL. Lo podés mandar a alguien y ve tu pizarrón sin necesidad de servidor. *(Las imágenes no se comparten porque pesan demasiado para una URL.)*

Quien recibe el link ve un banner con dos opciones: **Copiar a mi canvas** (reemplaza el suyo) o **Cerrar vista** (vuelve al propio).

## Atajos de teclado

| Atajo | Acción |
|---|---|
| `H` | Mostrar / ocultar la barra lateral |
| `Ctrl+V` | Pegar imagen del portapapeles |
| `Doble clic` | Editar texto / evento / checklist |
| `Delete` / `Backspace` | Borrar el elemento seleccionado |
| `Escape` | Deseleccionar o cerrar modal |

## Uso

Abrir `index.html` en el navegador. No hay nada más que hacer.

## Deploy

Funciona en cualquier hosting estático (GitHub Pages, Vercel, Netlify) o directamente desde el filesystem.

Para publicarlo en GitHub Pages:

1. Subir el repo a GitHub.
2. En **Settings → Pages**, elegir branch `main` y carpeta `/ (root)`.
3. La página queda disponible en `https://<usuario>.github.io/<repo>/`.

## Tech

Un único archivo `index.html` con HTML, CSS y JavaScript vanilla. Sin dependencias, sin build, sin servidor. Los datos del canvas viven en `localStorage` y los links de compartir codifican el estado en base64 url-safe dentro del query param `?c=`.

