# Proyecto: Calidad del aire por estación y hora en Bogotá

## Pregunta de análisis
¿Cómo varía la concentración de material particulado (PM10 y PM2.5) por estación de monitoreo y por hora del día en Bogotá, y qué franjas horarias concentran los mayores picos de contaminación? La respuesta sirve para identificar horas críticas en las que conviene restringir actividades al aire libre o regular el tráfico vehicular.

## Fuente de datos
Red de Monitoreo de Calidad del Aire de Bogotá (RMCAB), operada por la Secretaría Distrital de Ambiente. Los datos se publican en el portal de Datos Abiertos de Bogotá: https://datosabiertos.bogota.gov.co/. Licencia: Creative Commons Attribution 4.0. Frecuencia de actualización: horaria, con históricos anuales disponibles.

## Variables previstas
- `fecha_hora`: marca temporal de la medición (resolución horaria).
- `estacion`: nombre de la estación de monitoreo.
- `pm10`: concentración de material particulado menor a 10 micrómetros (µg/m³).
- `pm25`: concentración de material particulado menor a 2.5 micrómetros (µg/m³).
- `temperatura`: temperatura ambiente en grados Celsius.
- `humedad`: humedad relativa en porcentaje.
- `viento`: velocidad del viento en m/s.

## Herramientas del curso
- **pandas**: para limpiar, filtrar y agregar las mediciones horarias por estación y franja del día.
- **PySpark**: si el volumen de datos crece (varios años de series horarias), para procesar los agregados en paralelo.
- **Docker**: para fijar versiones exactas de las bibliotecas y garantizar que los resultados se reproduzcan igual en cualquier máquina.
- **Databricks / Cassandra**: se consideran para almacenar los agregados por hora y estación en un proyecto en producción.

