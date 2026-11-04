# MelodIA

**Tu cancionero inteligente: crea, guarda y comparte canciones con IA.**

MelodIA genera portadas cuadradas, letras y canciones a partir de un genero, una voz y una descripcion o tema. El resultado puede descargarse como una cancion individual o como una grilla HTML interactiva.

## Caracteristicas

- Generacion de portadas cuadradas bajo demanda.
- Selector de 15 estilos visuales, incluyendo vintage, cartoon 3D, anime, acuarela y cyberpunk.
- Selector de idioma para generar la interfaz, la letra y la cancion en español o inglés.
- Genero personalizado mediante un cuadro de dialogo.
- Generacion musical con `google/lyria-3-clip-preview` mediante Pollinations AI.
- Selector de modelo de audio entre `google/lyria-3-clip-preview` y `google/lyria-3.5`.
- Generacion de letra antes del audio; la letra se incluye en el prompt enviado a Lyria.
- Pollinations AI como proveedor unico.
- Persistencia local de la API key de Pollinations AI.
- Descarga de canciones en formato MP4 cuando el navegador admite `MediaRecorder` con MP4.
- Descarga de una grilla HTML con una tarjeta por cancion.
- Portada individual para cada tarjeta de la grilla.
- Reproductor independiente por tarjeta, con un solo video activo a la vez.
- Las grillas existentes no usan una portada compartida: cada video muestra su propio primer fotograma al cargarse.
- Letra editable debajo de la portada para regenerar el MP4 con una version modificada.
- Boton **Subir imagen** para reemplazar la portada generada y actualizar el MP4 actual.

## Archivos principales

- `index.html`: aplicacion para generar portadas, canciones y grillas.
- `grilla.html`: grilla HTML generada y lista para abrir en el navegador.
- `ejemplo.html`: ejemplo de grilla de imagenes.
- `imagen.png`, `propiedades.png` y `gifanimadoRedProyecto.gif`: recursos visuales del proyecto.
- `Bajo_la_luna_del_cafetal.mp4`: recurso multimedia de prueba.

## Uso

1. Abre `index.html` en un navegador moderno.
2. Introduce y valida tu API key de Pollinations AI.
3. Selecciona el idioma, genero y voz.
4. Escribe la descripcion o el tema de la cancion.
5. Selecciona uno de los 15 estilos visuales.
6. Selecciona el modelo de audio: `google/lyria-3-clip-preview` o `google/lyria-3.5`.
7. Pulsa **Generar Nueva** para crear la portada, la letra y el audio.
8. Edita la letra debajo de la portada y pulsa **Regenerar con esta letra** para crear otra version.
9. Pulsa **Descargar cancion** para guardar el MP4 actual.
10. Pulsa **Descargar grilla** para generar un HTML con todas las canciones creadas.
11. Abre el HTML descargado y usa **Play** en cualquier tarjeta.

## Reproduccion y compatibilidad

El boton **Play** reproduce la tarjeta seleccionada y detiene las demas. El audio no se silencia automaticamente. Si el navegador no puede reproducir un MP4 concreto, la grilla conserva el boton en **Play** y muestra un aviso.

Para obtener mejores resultados, usa una version actualizada de Chrome o Edge. Si el archivo se abre directamente desde el sistema y el navegador aplica restricciones a recursos locales, sirve la carpeta con un servidor HTTP local.

## Solucion de problemas

- **No se ven las portadas:** comprueba que el HTML se haya descargado completo y que las tarjetas incluyan su atributo `poster` o su primer fotograma de video.
- **Todos los videos muestran la misma imagen:** elimina cualquier `poster="imagen.png"` compartido de una grilla antigua. La version actual no usa ese poster común.
- **Play no inicia:** confirma que el archivo MP4 sea válido y prueba con Chrome o Edge actualizado.
- **No se puede generar:** revisa la API key de Pollinations AI y la conexion de red.

## Creditos

Disenado por **Juan Guillermo Rivera Berrio** con tecnologia Gemini 3 y asistencia de Antigravity.

Este proyecto forma parte de una serie de herramientas creativas desarrolladas para la exploracion artistica con IA en 2026.
