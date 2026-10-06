# Roma 2026 · Cuenta atrás + guía diaria

Web estática responsive para el viaje a Roma del 17 al 22 de octubre de 2026.

## Incluye
- Portada con cuenta atrás.
- Navegación por días.
- Resumen de cada jornada.
- Mapa interactivo por día con puntos numerados y trazado orientativo.
- Lista ordenada de paradas vinculada al mapa.
- Botón para abrir la ruta en Google Maps.
- Tarjetas con fotografía, hora y explicación breve de cada sitio.
- Diseño optimizado para móvil.

## Mapas
Los mapas usan Leaflet + OpenStreetMap. Necesitan conexión a Internet para cargar las teselas del mapa. La línea mostrada en la web une las paradas de forma orientativa y no pretende ser una ruta peatonal giro a giro.

## Despliegue
Proyecto estático: subir todo el contenido a la raíz del repositorio conectado a Vercel. No necesita build, backend ni dependencias npm.


## Actualización: mapas estáticos y contador con segundos
- Se eliminó Leaflet/OpenStreetMap interactivo de la interfaz.
- Cada jornada tiene ahora un mapa estático local con puntos numerados y clicables.
- Los días del centro histórico usan recortes locales del mapa aportado por el usuario; llegada/salida usan un mapa regional estilizado.
- El botón “Ver ruta en Google Maps” se mantiene para navegación real.
- El contador muestra días, horas, minutos y segundos.
- Se añadieron al resumen visual varias ubicaciones explícitas que estaban en el itinerario y no aparecían como paradas independientes.

Actualización mapas móviles
- Eliminados los bloques visuales "Mapa premium", "Tarjeta de ruta" y "Mini leyenda".
- Mapas estáticos regenerados en proporción 4:3 y optimizados para smartphone.
- El recorrido se dibuja en el propio mapa y la web mantiene marcadores interactivos superpuestos.
- Al pulsar una parada se resalta su marcador y se actualiza la parada seleccionada.
- Se mantiene el botón de ruta en Google Maps.
- Orden de paradas revisado respecto al itinerario: especialmente Vaticano/Prati y el regreso del jueves.


## Mejora móvil de mapas
- El mapa mantiene su proporción original y ya no se deforma con `object-fit: fill`.
- En smartphone, los mapas urbanos se muestran en un viewport casi cuadrado con recorte/zoom visual sin perder la alineación de los marcadores.
- Vaticano/Prati recibe un zoom móvil específico por la concentración de paradas.
- Los mapas de traslado (Fiumicino ↔ Roma) usan una proporción 5:4 para conservar aeropuerto y centro en la misma vista.
- La información de la parada seleccionada aparece debajo del mapa.
- Los marcadores son más pequeños en móvil y conservan resaltado interactivo.
- Botón para ampliar el mapa en un diálogo y botón directo a Google Maps.
- Las tarjetas de lugares también permiten seleccionar/resaltar la parada correspondiente.
