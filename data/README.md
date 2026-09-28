# 📖 Diccionario de datos

Archivo: `processed/ladb_mobility_economy_2024_clean.csv`
Granularidad: una fila por ciudad (15 ciudades, año 2024).

## Variables de movilidad (fuente: TomTom Traffic Index, promedio anual 2024)

| Columna | Descripción |
| --- | --- |
| `city` | Nombre estandarizado de la ciudad |
| `country` | Código ISO-3 del país |
| `year` | Año de análisis (2024) |
| `jams_delay` | Retraso total (minutos) provocado por la congestión en las vías monitoreadas. Depende del tamaño de la ciudad |
| `traffic_index_live` | Índice de tráfico (0–100). Valores altos indican más congestión |
| `jams_length_in_kms` | Longitud total de los embotellamientos (km) |
| `jams_count` | Número de embotellamientos activos |
| `mins_delay` | Minutos de retraso promedio por cada 10 km frente a condiciones sin congestión |
| `travel_time_live_per_10kms_mins` | Tiempo de viaje actual para recorrer 10 km (minutos) |
| `travel_time_historic_per_10kms_mins` | Tiempo de viaje histórico para 10 km (minutos) |

## Variables económicas (fuente: OECD Cities, 2024)

| Columna | Descripción |
| --- | --- |
| `city_gdp_capita` | PIB per cápita (USD) |
| `unemployment_perc` | Tasa de desempleo (%) |
| `pm25_ug_m3` | Concentración media anual de PM2.5 (µg/m³). **Nota:** conserva coma decimal como texto; no se usó en el análisis |
| `population` | Población total (habitantes) |

## Notas

- Los archivos originales de TomTom (~1 millón de registros) no se incluyen por su tamaño.
- El PIB per cápita de Santiago (2,277 USD) parece atípico y debe verificarse contra la fuente original.
