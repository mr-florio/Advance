# Avance del año

Una página web simple que muestra qué porcentaje del año transcurrió.

## ¿Para qué?

En muchos lugares de trabajo se dibuja a mano en un pizarrón una barra que indica cuánto del año ya pasó, y la cuenta se hace manualmente cada vez. Esta página automatiza esa tarea.

## Qué muestra

- Porcentaje del año con dos decimales
- Barra de progreso visual
- Días transcurridos y días restantes
- Fecha actual en español

Se actualiza solo cada minuto.

## Uso

Abrir `index.html` en el navegador. No hay nada más que hacer.

## Deploy

Funciona en cualquier hosting estático (GitHub Pages, Vercel, Netlify) o directamente desde el filesystem.

Para publicarlo en GitHub Pages:

1. Subir el repo a GitHub.
2. En **Settings → Pages**, elegir branch `main` y carpeta `/ (root)`.
3. La página queda disponible en `https://<usuario>.github.io/<repo>/`.

## Tech

Un único archivo `index.html` con HTML, CSS y JavaScript vanilla. Sin dependencias, sin build, sin servidor.
