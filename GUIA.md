# Taller de misiones para HeroQuest

Editor estático en español. Versión 1.2, 19 de octubre de 2026.

## Empezar en un ordenador

1. Extrae el ZIP completo.
2. Abre `index.html` en Chrome, Edge, Firefox o Safari actualizado. No necesita instalación, conexión, cuenta ni servidor.
3. Elige Clásico o Cara B en Mapa. Cada tablero conserva su misión por separado. Elige una pieza y toca una casilla; las puertas se colocan tocando un muro.
4. Pulsa **Guardar JSON** para conservar una copia editable o **Descargar PDF** para obtener el imprimible.

Se entrega también `HeroQuest-editor.html`, un archivo autónomo con todo incorporado: basta abrirlo. La carpeta con archivos separados es más cómoda para modificar o publicar el editor.

## Crear y editar

- Seleccionar: toca una pieza y después un destino libre. El destino corresponde a la esquina superior izquierda de su huella.
- Girar: rota una pieza seleccionada o la siguiente que colocarás. En puertas cambia el lado de apertura manteniendo el muro.
- Borrar: activa la goma y toca la pieza; también puedes borrar una pieza seleccionada.
- Deshacer y rehacer: hasta 150 cambios de piezas o textos durante la sesión. Cargar JSON y comenzar una misión nueva también se pueden deshacer.
- Los muebles no pueden cruzar paredes, superponerse con otras piezas ni salirse del tablero. Una nota puede compartir casilla con una pieza. No se valida el equilibrio de la misión ni si todas las salas son accesibles.
- Las notas A, B, C… se colocan desde **Héroes y notas**; el texto correspondiente se escribe en el panel opcional **Misión completa**.
- El ejemplo `ejemplo-mision.json` permite explorar el editor sin empezar de cero.

## Tablet y teclado

**Táctil** amplía las casillas a un mínimo de 44 píxeles. Desliza para recorrer el mapa y toca para colocar. Los controles tienen una altura mínima de 44 píxeles. Ajustar vuelve a una vista general. No se requiere arrastrar piezas ni hacer gestos precisos.

Enfoca el tablero con Tab: flechas para escoger casilla, Enter o Espacio para actuar, R para girar, Suprimir para borrar y Escape para soltar. Ctrl/Cmd+Z deshace y Ctrl/Cmd+Mayús+Z rehace. Las puertas se ajustan al muro próximo a la casilla elegida; en esquinas, usar un toque sobre el muro permite elegir el segmento exacto.

En tablet, la forma más fiable de abrirlo es mediante una página estática como GitHub Pages. La apertura directa de HTML desde la aplicación Archivos depende de las restricciones de iOS/Android; algunas vistas previas de archivos no ejecutan JavaScript. No se ha probado en hardware físico de tablet.

## Guardado

La última misión de cada tablero se guarda automáticamente en el almacenamiento de este navegador. Depende del dispositivo, perfil, URL y permisos del navegador; no se sincroniza. El modo privado o los archivos locales pueden restringirlo. Si no está disponible, se muestra **Sin autoguardado · usa Guardar JSON**. Guarda JSON para tener una copia duradera o cambiar de dispositivo. No mantengas dos pestañas editando la misma misión: se avisa si otra pestaña cambia el guardado.

Abrir JSON valida el formato, las piezas y sus posiciones antes de sustituir la misión. Los archivos de otros editores no son compatibles. El JSON identifica el mapa y recupera el tablero correspondiente al abrirlo.

## Compartir una misión

1. Pulsa **Compartir misión**. Se prepara una copia del tablero, las piezas y todos los textos.
2. Pulsa **Enviar enlace…** y elige WhatsApp, correo u otra aplicación disponible. Si el navegador no admite ese menú, usa **Copiar enlace**, pégalo en un mensaje y envíalo.
3. Quien reciba el enlace pulsa **Abrir misión** para continuar editándola. Antes puede guardar la misión que ya tenía. La apertura se puede deshacer.

No necesita cuenta y no sube las misiones al repositorio. La copia está dentro del enlace: cualquiera que lo reciba puede abrirla. No se sincroniza; después de editar, comparte un enlace nuevo. En un móvil prestado, recuerda enviar el mensaje antes de devolverlo. Cancelar el menú de compartir no envía ni conserva una copia en otro dispositivo.

Los enlaces apuntan a la web pública del editor. Para abrir enlaces comprimidos se necesita un navegador actualizado. Si una misión es demasiado larga para un enlace fiable, se avisa y se ofrece Guardar JSON sin recortar contenido. Las aplicaciones de mensajería pueden imponer sus propios límites; guarda JSON para copias de archivo.

## PDF e impresión

**Descargar PDF** produce directamente un PDF vectorial en blanco y negro, A4 horizontal y con casillas cuadradas. Sin introducción, objetivos ni notas genera una sola hoja; el título, si existe, se imprime en esa hoja. Solo se añaden páginas cuando se escribe alguno de esos textos. Las notas largas se paginan automáticamente. El PDF usa fuentes estándar: se admiten los caracteres españoles habituales; evita emojis y alfabetos no latinos en los textos destinados a PDF.

**Imprimir** ofrece la impresión del navegador como alternativa. Selecciona A4, horizontal, escala 100 % y desactiva encabezados y pies del navegador. Algunos navegadores o impresoras sustituyen los márgenes; la descarga directa de PDF evita esa variación.

## Tableros y fidelidad

Incluye dos mapas:

- **Clásico:** 26 × 19 casillas y 22 salas, con el entrante de la sala sureste. Geometría contrastada con la fuente indicada abajo.
- **Cara B · El Despertar / First Light:** trazado del archivo `heroquest_caraB_A4.pdf` aportado y confirmado expresamente por el usuario como referencia correcta. Contiene 25 columnas y 19 franjas horizontales. La franja inferior comprimida de la imagen se regulariza a una fila completa, con todas las casillas cuadradas. Se conservan las conexiones, posiciones de los muros y 19 zonas delimitadas del PDF. La comparación automática con la imagen detectó los mismos 254 segmentos interiores, sin discrepancias. La fidelidad se refiere al PDF confirmado; no se cotejó con fotografías del tablero físico que no estaban disponibles.

Las paredes base son fijas. **Bloqueo** y **Bloqueo doble** ocupan una o dos casillas para cerrar el paso, como las losetas del juego. No existe una herramienta para dibujar una pared sin ocupar casillas, según lo acordado con el usuario.

## GitHub Pages

1. Crea un repositorio o usa uno de tu elección.
2. Sube el contenido de esta carpeta, incluyendo `vendor/`, a la raíz o a `docs/`.
3. En Settings → Pages, publica esa carpeta desde la rama elegida.
4. Abre la dirección que indique GitHub Pages en el ordenador o tablet.

No requiere proceso de compilación, rutas absolutas, claves ni backend. También puede alojarse en cualquier servidor estático. Para una publicación mínima puedes renombrar el archivo autónomo `HeroQuest-editor.html` a `index.html` y subirlo solo.

## Fuentes y licencias

Geometría clásica contrastada y adaptada de **Heroquest board.svg**, de **CMG Lee**, [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Heroquest_board.svg), licencia [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Cambios: representación de salas como polígonos, segmentación de paredes y supresión de texturas. La geometría derivada conserva CC BY-SA 4.0. La plantilla clásica adjunta por el usuario también se usó para el contraste.

Código de la aplicación e iconos originales: licencia MIT, ver `LICENSE.txt`. No se reutilizan iconos oficiales. HeroQuest y los nombres del juego pertenecen a sus titulares. Proyecto de aficionados no oficial, sin afiliación a Hasbro.

Bibliotecas incluidas localmente: jsPDF 3.0.3 y svg2pdf.js 2.6.0, licencias MIT en `vendor/`. No se cargan recursos desde Internet al usar el editor.

## Verificación

218 comprobaciones de lógica superadas. Se probaron en navegador la colocación, puertas en muros, movimiento, rotación, deshacer/rehacer, cambio de mapa sin perder la misión, guardar/abrir JSON, recuperar tras recarga y descargar PDF. Vista de tablet de 1024 × 768 comprobada, con casillas táctiles mayores de 44 píxeles. PDF rápido: una página A4 horizontal; misión con notas: dos páginas; 100 notas: cinco páginas con la última nota presente. Ambas salidas se revisaron visualmente.

La apertura mediante `file://` no pudo probarse en el navegador automatizado porque su política solo permite HTTP/HTTPS. El archivo autónomo no tiene dependencias remotas, módulos, peticiones de red ni un proceso de instalación; sus cuatro scripts incrustados se comprobaron sintácticamente. No se probó Safari/iPad físico ni una impresora física. Para ese uso, se recomienda comprobar una misión pequeña antes de preparar una sesión completa.
