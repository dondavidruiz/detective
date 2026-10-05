# Agencia de Detectives Lectores

App web de retos progresivos de comprensión lectora para 4.º de Primaria.
El alumno escribe su nombre y resuelve 10 casos de detective, de acertijos a lectura crítica.
Para pasar al caso siguiente tiene que superar el anterior.

Autor: David Ruiz - 2026

## Contenido

- `index.html`: la app completa en un solo archivo, sin instalaciones ni servidor.

## Publicar en GitHub Pages

1. Entra en GitHub y crea un repositorio nuevo, por ejemplo `detectives-lectores`. Márcalo como **Public**.
2. Pulsa **Add file → Upload files**, arrastra `index.html` y `README.md` y pulsa **Commit changes**.
3. Ve a **Settings → Pages**.
4. En **Source**, elige **Deploy from a branch**. En **Branch**, elige `main` y la carpeta `/ (root)`. Pulsa **Save**.
5. Espera uno o dos minutos. La app quedará disponible en
   `https://TU-USUARIO.github.io/detectives-lectores/`

## Dónde se guarda el progreso

Esta versión guarda el progreso **en el navegador del dispositivo** (localStorage):

- Si el alumno siempre usa la misma tablet u ordenador, solo tiene que escribir el mismo nombre para seguir donde lo dejó.
- La **Zona del profesorado** muestra el alumnado que ha jugado en **ese** dispositivo.
- El progreso se pierde si se borran los datos del navegador o si se usa el modo incógnito.

## Zona del profesorado

- El PIN inicial es **1234**. Cámbialo la primera vez que entres (botón *Cambiar PIN*).
- El PIN evita que el alumno entre por error, pero no es una protección fuerte, porque se guarda en el propio navegador.

## Cómo añadir o cambiar textos

Abre `index.html` con un editor de texto y busca `BANCO DE RETOS`. Cada nivel tiene sus textos (`casos`) con 5 preguntas:

- La respuesta correcta es siempre **la primera opción** de la lista `o`. La app baraja las opciones al mostrarlas.
- `pista` es la ayuda que aparece si el alumno falla.
- `exp` es la explicación que aparece al resolver la pregunta.
- `par` es el número del párrafo donde está la respuesta, contando desde 0. Si no corresponde a un párrafo concreto, pon `null`.

Copia un caso, cámbiale el `id` y el contenido, guarda el archivo y vuelve a subirlo a GitHub.

## Protección de datos

La app solo guarda el nombre o apodo y los resultados de lectura. No introduzcas apellidos ni otros datos personales.
