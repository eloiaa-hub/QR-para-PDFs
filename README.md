# QR-PDF · Generador de QR para partituras

Añade un código QR con el enlace a un audio (por ejemplo, un MP3 subido a internet) sobre una partitura en PDF. Quien tenga la partitura impresa escanea el código con el móvil y escucha la obra.

**Usarlo en línea:** https://eloiaa-hub.github.io/QR-para-PDFs/

![El programa con una partitura abierta](img/programa.png)

## Características

- **Sin conexión:** es un único archivo HTML (`QR-PDF.html`). Se descarga y se abre con doble clic, sin instalar nada.
- **Privado:** las partituras no salen del ordenador.
- **Calidad de imprenta:** el QR se añade como dibujo vectorial; el resto del PDF no se modifica ni pierde calidad. Se guarda siempre una copia (`nombre_QR.pdf`) y el original no cambia.
- **Vista previa:** el QR se arrastra, se redimensiona y se coloca con precisión en milímetros o con las flechas del teclado.
- **Junto al título:** coloca el QR automáticamente a la izquierda del título de cada partitura.
- **Varias partituras a la vez:** se pueden abrir muchas juntas y guardarlas en un ZIP con el QR en la misma posición.
- **Dirección base y `{nombre}`:** cada partitura enlaza sola con su audio (`Ave Maria.pdf` → `…/audios/Ave%20Maria.mp3`). Una tabla de enlaces permite cambiar el de una sola partitura, e importar o exportar la lista en CSV.
- **Varios QR por partitura:** hasta 8 (por movimiento, por voz…), cada uno con su enlace, su texto y su página (primera, última, todas o una concreta).
- **Tipos de QR:** enlace web, texto, wifi, contacto (vCard), correo, teléfono, SMS, WhatsApp, ubicación (Google Maps) y evento de calendario. La contraseña del wifi no se guarda en el navegador.
- **Audio desde un momento concreto:** «Empieza en» y «Termina en» (min:seg) añaden `#t=` al enlace, para que cada QR lleve a su movimiento dentro de un mismo MP3.
- **Texto sin conexión:** un QR de texto se lee sin internet (letra traducida, notas, indicaciones), con contador de caracteres.
- **Texto junto al QR:** debajo o al lado (bloque apaisado), por ejemplo «Escuchar · Ave Maria», con un icono de altavoz si se quiere.
- **Avisos:** marca en rojo los QR que tapan notas, texto o pentagramas, o que se solapan entre sí, y avisa si el QR queda demasiado pequeño.
- **Comprobación:** al guardar vuelve a leer cada QR del PDF nuevo y confirma que lleva el enlace correcto.
- **Posiciones guardadas:** guarda colocaciones con nombre («A4 vertical», «Coro SATB»…) y llévalas a otro ordenador con un archivo JSON.
- **Hoja de pegatinas:** crea un PDF con los QR para papel adhesivo, con plantillas habituales (Apli / Avery) o medidas propias.
- **Otros:** el QR puede abrir el enlace al pulsarlo en pantalla, se exporta en PNG o SVG, hay tema claro y oscuro, y ayuda integrada.

## Uso rápido

1. Pega el enlace del MP3 (o escribe la dirección base si vas a hacer varias partituras).
2. Abre o arrastra las partituras en PDF.
3. Coloca el QR, por ejemplo con **Junto al título**.
4. Pulsa **Guardar PDF con el QR** o **Guardar las partituras (ZIP)**.

## Manual

- [Manual en HTML](manual.html)
- [Manual en PDF](manual.pdf)

## Archivos

| Archivo | Contenido |
|---|---|
| `QR-PDF.html` | El programa completo (incluye todas las bibliotecas) |
| `index.html` | Página de presentación para GitHub Pages |
| `manual.html` · `manual.pdf` | Manual de uso |
| `img/` | Capturas usadas en la página y el manual |

## Bibliotecas incluidas

`QR-PDF.html` lleva dentro estas bibliotecas de código abierto para funcionar sin internet:

- [PDF.js](https://github.com/mozilla/pdf.js) 3.11 (Apache-2.0): muestra la partitura.
- [pdf-lib](https://github.com/Hopding/pdf-lib) 1.17 (MIT): añade el QR al PDF.
- [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) 2.0 (MIT): genera el código QR.
- [jsQR](https://github.com/cozmo/jsQR) 1.4 (Apache-2.0): lee los QR del PDF guardado para comprobarlos.

## Licencia

- **Programa** (`QR-PDF.html` e `index.html`): [EUPL-1.2](LICENSE), la Licencia Pública de la Unión Europea. Puedes usarlo, estudiarlo, modificarlo y redistribuirlo. Si distribuyes una versión modificada, debe seguir publicándose con la EUPL o con una licencia compatible.
- **Manual** (`manual.html`, `manual.pdf` y capturas de `img/`): [CC BY-SA 4.0](LICENSE-manual), Creative Commons Atribución-CompartirIgual 4.0 Internacional. Puedes copiarlo y adaptarlo citando la autoría y compartiendo las obras derivadas con la misma licencia.
- Las bibliotecas incluidas conservan sus propias licencias (Apache-2.0 y MIT).

© 2026 Eloi A.A.
