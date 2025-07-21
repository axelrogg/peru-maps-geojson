# 🇵🇪 Límites Administrativos del Perú (GeoJSON)

Este repositorio contiene archivos **GeoJSON actualizados** (al año 2023,
según el INEI) con las **divisiones administrativas del Perú**:

- **Departamentos**
- **Provincias**
- **Distritos**

---

## 📁 Archivos

| Nivel        | Nombre del archivo    | Descripción      |
|--------------|-----------------------|------------------|
| Departamento | `departments.geojson` | 25 departamentos |
| Provincia    | `provinces.geojson`   | 196 provincias   |
| Distrito     | `districts.geojson`   | 1891 distritos   |

Todos los archivos usan la proyección **WGS 84 (EPSG:4326)**.

## 📑 Propiedades de los archivos GeoJSON

### 🗺️ Departamentos

| Propiedad    | Tipo                                    | Descripción                                |
|--------------|-----------------------------------------|--------------------------------------------|
| `code`       | string                                  | Código de 2 dígitos del departamento.                   |
| `name`       | string                                  | Nombre del departamento.                   |
| `length_deg` | float                                   | Longitud del perímetro en grados           |
| `area_deg`   | float                                   | Superficie en grados cuadrados.            |
| `length_km`  | float                                   | Longitud del perímetro en kilómetros.      |
| `area_km2`   | float                                   | Superficie en kilómetros cuadrados.        |
| `geometry`   | Polygon/MultiPolygon/GeometryCollection | Representa la forma geográfica del objeto. |


### 🏙️ Provincias

| Propiedad         | Tipo                                    | Descripción                                                         |
|-------------------|-----------------------------------------|---------------------------------------------------------------------|
| `code`            | string                                  | Código de 4 dígitos de la provincia.                                |
| `department_code` | string                                  | Código de 2 dígitos del departamento al que pertenece la provincia. |
| `department_name` | string                                  | Nombre del departamento al que pertenece la provincia.              |
| `name`            | string                                  | Nombre de la provincia.                                             |
| `length_deg`      | float                                   | Longitud del perímetro en grados                                    |
| `area_deg`        | float                                   | Superficie en grados cuadrados.                                     |
| `length_km`       | float                                   | Longitud del perímetro en kilómetros.                               |
| `area_km2`        | float                                   | Superficie en kilómetros cuadrados.                                 |
| `geometry`        | Polygon/MultiPolygon/GeometryCollection | Representa la forma geográfica del objeto.                          |


### 🏘️ Distritos

| Propiedad         | Tipo                                    | Descripción                                                         |
|-------------------|-----------------------------------------|---------------------------------------------------------------------|
| `code`            | string                                  | UBIGEO del distrito.                                                |
| `department_id`   | string                                  | Código de 2 dígitos del departamento al que pertenece el distrito.  |
| `department_name` | string                                  | Nombre del departamento.                                            |
| `province_code`   | string                                  | Código de 4 dígitos de la provincia a la que pertenece el distrito. |
| `province_code`   | string                                  | Nombre de la provincia.                                             |
| `name`            | string                                  | Nombre del distrito.                                                |
| `capital`         | string                                  | Capital del distrito.                                               |
| `length_deg`      | float                                   | Longitud del perímetro en grados                                    |
| `area_deg`        | float                                   | Superficie en grados cuadrados.                                     |
| `length_km`       | float                                   | Longitud del perímetro en kilómetros.                               |
| `area_km2`        | float                                   | Superficie en kilómetros cuadrados.                                 |
| `geometry`        | Polygon/MultiPolygon/GeometryCollection | Representa la forma geográfica del objeto.                          |

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

