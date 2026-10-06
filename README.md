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
