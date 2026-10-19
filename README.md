# Taller de misiones para HeroQuest

Editor web en español para crear misiones en ordenador, tablet o móvil.

**[Abrir el editor](https://5n7t99rb9d-web.github.io/heroquest-editor/)**

Elige un tablero, coloca las piezas y descarga tu misión como JSON editable o PDF A4 horizontal. No necesitas crear una cuenta para usarlo.

- Tablero clásico y cara B de El Despertar / First Light, trazada del PDF de referencia confirmado por el propietario del proyecto.
- 35 tipos de piezas, puertas ajustadas a muros, giro, borrado, deshacer y rehacer.
- Modo táctil con casillas de al menos 44 píxeles y edición por teclado.
- Textos opcionales: título, introducción, objetivos y notas de salas.
- Guardado local independiente para cada tablero. Las misiones no se envían a un servidor ni se sincronizan entre dispositivos; usa Guardar/Abrir JSON para trasladarlas.
- PDF vectorial en blanco y negro: una hoja sin notas; páginas adicionales solo cuando hay textos.

Consulta la [guía de uso](GUIA.md). Puedes descargar `index.html` y abrirlo localmente en un navegador moderno; todas las bibliotecas están incorporadas.

## Desarrollo y alojamiento

Aplicación estática sin backend, servicios de pago ni proceso de compilación. GitHub Pages publica la rama `main`, carpeta raíz. Para actualizar, sustituye `index.html` por una versión nueva. La web conserva las misiones locales mientras se mantenga su dirección y el almacenamiento del navegador.

## Créditos

Proyecto de aficionados no oficial, sin afiliación a Hasbro. HeroQuest pertenece a sus titulares. Iconos originales.

Geometría clásica adaptada de [Heroquest board.svg, CMG Lee](https://commons.wikimedia.org/wiki/File:Heroquest_board.svg), bajo CC BY-SA 4.0. La cara B reproduce la disposición del PDF aportado y confirmado por el propietario; la franja inferior comprimida se regularizó para obtener casillas cuadradas.

Código e iconos: [MIT, con la excepción de la geometría indicada](LICENSE.txt). Bibliotecas incorporadas: jsPDF y svg2pdf.js, [licencias MIT](THIRD-PARTY-LICENSES.txt).
