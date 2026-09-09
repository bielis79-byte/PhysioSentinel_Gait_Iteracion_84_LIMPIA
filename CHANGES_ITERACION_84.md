# PhysioSentinel Gait · Iteración 84

## Cambio principal
Se ralentiza de forma deliberada la cámara virtual de los vídeos 3D multivista para favorecer el análisis visual.

- La secuencia clínica mantiene mesetas de observación en frontal, lateral, posterior y superior.
- Las transiciones entre vistas ocupan más tiempo y usan interpolación suave (`smoothstep`).
- El ciclo de marcha se repite tres veces durante el render multivista, desacoplando la velocidad de la cámara de la duración de un único ciclo.
- La órbita continua también se ralentiza, incorpora pausas breves al atravesar vistas cardinales y termina con transición hacia vista superior.
- Se conservan escala, límites XYZ y centro espacial durante todo el vídeo.
- El resultado sigue siendo descargable como MP4 e integrable en la exportación ZIP.

## Sin cambios biomecánicos
No se modifican cálculos 2D/3D, tracking, segmentación temporal, métricas, Supabase ni convenciones clínicas. V84 cambia únicamente el renderizado de cámara del vídeo 3D multivista.
