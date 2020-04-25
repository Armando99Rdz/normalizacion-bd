# Normalización de Bases de Datos
april 24th, 2020

## Acrónimos / Definiciones
- DB/BD: Database / Base de datos
- FN: Forma normal
- 1FN: Primera forma normal
- 2FN: Segunda forma normal
- 3FN: Tercera forma normal
- Entidad: Refiere a una colección de datos, sinónimo de *tabla*.

## Definición de Normalización BD
Directamente **es la forma/proceso de organizar la información en una Base de Datos**. Para ello debemos tomar en cuenta la *Creación* de tablas y sus *Relaciones*.


## ¿Para qué?
- Disminuir la redundancia de datos
- Mejor interpretación
- Optimización de tiempos
- Proteger integridad de los datos
- Escalabilidad
- Prevención de errores


## Normalizar 
Para normalizar una base de datos es necesario cumplir con las siguientes reglas:
- Cada entidad con nombre único
- Erradicar filas idénticas dentro de la misma entidad
- Todos los valores de una columna del mismo tipo de dato


## Niveles de Normalización
Principalmente existen **3 conjuntos de reglas** para normalizar una Base de Datos (aunque existen niveles superiores, una BD al tercer nivel se considera en óptimo estado). A este conjunto de reglas se les conoce como; **primera forma normal**, **segunda forma normal** y **tercer forma normal**.


## 1FN : Primera forma normal
Transformar una entidad a la primera forma normal consiste en:
- Eliminar grupos idénticos de tablas individuales
- Creación de tablas separadas para cada conjunto de datos relacionados
- Identificación de cada conjunto de datos con una clave primaria.

### Resultados
Si la 1FN es aplicada correctamente, la entidad debe cumplir y resultar con:

    - Datos atómicos
    - Una columna para claves primarias
    - Columna de claves primaria no permite nulos
    - Los no claves primarias dependen de y sólo de la clave primaria
    - Independencia del orden tanto de filas como de columnas
## 2FN: Segunda forma normal
Seguir los siguientes pasos para cumplir con la 2FN.
- Crear tablas individuales para valores que aplican varios registros.
- Relacionar estas tablas con una clave externa/foránea

### Resultados 
Deducirémos que la tabla aplica con la 2FN si ésta cumple con:

    - La 1FN
    - Atributos dependen completamente de la clave primaria
    - No dependencias parciales
## 3FN: Tercer forma normal
Cumplir con los siguientes para convertir una tabla en 2FN a 3FN.
- Eliminar campos que no dependan de la clave primaria
- No puede haber datos derivados

### Resultados
    - Cumple con 2FN
    - Ninguna dependencia entre los no claves primaria

## Otras formas de normalización
Existen otros niveles superiores de normalización de Boyce Codd pero rara vez se considera en un diseño práctico. Si no se tienen en cuenta estas normas, se considera una base de datos casi perfecta, por lo que, cumplir con la primera, segunda y tercer forma normal no afecta a la funcionalidad de las aplicaciones actuales.