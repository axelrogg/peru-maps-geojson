# 🇵🇪 Límites Administrativos del Perú (GeoJSON)

Este repositorio contiene archivos **GeoJSON actualizados** (al año 2023, según el INEI) con las **divisiones administrativas del Perú**:

- **Departamentos**
- **Provincias**
- **Distritos**

Estos archivos son adecuados para su uso en:
- Mapas web (por ejemplo, Leaflet, Mapbox, D3.js)
- Herramientas GIS (por ejemplo, QGIS, ArcGIS)
- Análisis de datos o proyectos de tecnología cívica

---

## 📁 Archivos

| Nivel        | Nombre del archivo     | Descripción      |
|--------------|------------------------|------------------|
| Departamento | `departments.geojson` | 24 departamentos |
| Provincia    | `provinces.geojson`   | 193 provincias   |
| Distrito     | `districts.geojson`   | 1621 distritos   |

Todos los archivos usan la proyección **WGS 84 (EPSG:4326)**.

## 📑 Propiedades de los archivos GeoJSON

### 🗺️ Departamentos

| Propiedad  | Tipo         | Descripción                                          |
|------------|--------------|------------------------------------------------------|
| `id`       | string       | UBIGEO del departamento.                             |
| `name`     | string       | Nombre del departamento.                             |
| `length`   | string       | Longitud del perímetro en grados (latitud/longitud). |
| `area`     | string       | Área superficial en grados cuadrados.                |
| `geometry` | MultiPolygon | Representa la forma geográfica del objeto.           |


### 🏙️ Provincias

| Propiedad         | Tipo         | Descripción                                            |
|-------------------|--------------|--------------------------------------------------------|
| `id`              | string       | UBIGEO de la provincia.                                |
| `department_id`   | string       | UBIGEO del departamento al que pertenece la provincia. |
| `department_name` | string       | Nombre del departamento al que pertenece la provincia. |
| `name`            | string       | Nombre de la provincia.                                |
| `length`          | string       | Longitud del perímetro en grados (latitud/longitud).   |
| `area`            | string       | Área superficial en grados cuadrados.                  |
| `geometry`        | MultiPolygon | Representa la forma geográfica del objeto.             |


### 🏘️ Distritos

| Propiedad         | Tipo         | Descripción                                            |
|-------------------|--------------|--------------------------------------------------------|
| `id`              | string       | UBIGEO del distrito.                                   |
| `department_id`   | string       | UBIGEO del departamento al que pertenece el distrito.  |
| `department_name` | string       | Nombre del departamento.                               |
| `provincia_id`    | string       | UBIGEO de la provincia a la que pertenece el distrito. |
| `provincia_name`  | string       | Nombre de la provincia.                                |
| `name`            | string       | Nombre del distrito.                                   |
| `capital`         | string       | Capital del distrito.                                  |
| `length`          | string       | Longitud del perímetro en grados (latitud/longitud).   |
| `area`            | string       | Área superficial en grados cuadrados.                  |
| `geometry`        | MultiPolygon | Representa la forma geográfica del objeto.             |

## Notas

### Nombres de departamentos, provincias y distritos sin tildes

Los nombres de cada departamento, provincia y distrito carecen de tildaciones.
Esto es debido a que todos los nombres recogidos del INEI se encuentran
completamente en mayúsculas y sin tildes.

Trataré de ir actualizando los datos, pero esto tomará tiempo. Revisa la tabla
para saber si los datos están actualizados o no.

| Archivo       | Tildes añadidas |
|---------------|-----------------|
| Departamentos |       ❌        |
| Provincias    |       ❌        |
| Distritos     |       ❌        |

## Fuente

[INEI - Instituto Nacional de Estadística e Informática](https://ide.inei.gob.pe/#geo)

