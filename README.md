# Proyecto: Monitoreo del uso del suelo en la parroquia de San Antonio de Pichincha del Distrito Metropolitano de Quito.
Link code: https://colab.research.google.com/drive/1Fy6JawG_sK987rU5vMYMQbKHO2xXCi9r?usp=drive_link
---
## Preguntas orientadoras
*   ¿Cuales son las caracteristicas del uso del suelo?
*   ¿Cual es la densidad de lotes del suelo?
*   Con la disponibilidad de la data ¿Existe suelo vacante?
## Objetivos del Proyecto
### Objetivos general
*   Monitorear el uso del suelo en la parroquia de San Antonio de Pichincha del Distrito Metropolitano de Quito mediante el uso de tecnicas de ciencias de datos.
### Objetivos especifico
*   Identificar las librerias de python a usar para emplear datos espaciales.
*   Leer la informacion geoespacial mediante codigo de python.
*   Aplicar el tratamiento a la informacion geospacial mediante codigo de python.
*   Realizar un análisis exploratorio de datos espaciales mediante el uso de librerias de python.
*   Responder a la preguntas orientadoras para describir el estado del uso del suelo en la parroquia de San Antonio de Pichincha del Distrito Metropolitano de Quito.

---

### Fundamentos de ciencia de datos
Modulo 2 Proyecto
|   |   |
| :--- | :--- |
| **Autor:** | Ing. Diego F. Reyes Y. |
| **Fecha:** | octubre 2026 |
| **Fuente de Datos:** | Capa de Plan de Uso y Gestion del Suelo de la Secretaria de Hábitat y Ordenamiento Territorial https://gobiernoabierto.quito.gob.ec/ <br> Capa de Lotes - Catastro de la Secretaria General de Planificación https://geoportal.quito.gob.ec/geoportal/descargas.php <br>  Capa de Límite de Parroquias Rurales de la Secretaria General de Planificación https://geoportal.quito.gob.ec/geoportal/descargas.php|
---

# 1. Defincion del dominio del problema
Se esta realizando un estuido sobre el uso y aprovechamiento del suelo, la capacidad de fraccionamiento y la densidad de lotes en la  en la parroquia de San Antonio de Pichincha del Distrito Metropolitano de Quito
---

# 2. Adquisición y limpieza de datos

La adquisición de los datos parte de las fuentes oficiales, conforme a  la politica de datos abiertos.
Estos datos son:
*   catastro.gdb.zip
*   parroquia.gdb.zip
*   PUGS_2024.gdb.zip

 **Proceder a cargar la data al espacio de trabajo**
---
Instalación de librerias !pip install geopandas fiona shapely pyproj
---
Verificación de lectura de archivos
---
Revisión del sistema de referencia
---
Homogenización del sistema de referencia 
---
Visualización preliminar
Capa de ba003_uso_suelo_edificabilidad_a
Capa de LOTE
---
Identificación de área de estudio

Imprimir una muestra de 3 registros de la capa organizacion_territorial_parroquial_rural_a , para identificar campo que almacena la información del nombre de la parroquia
---
Lista de parroquias

Imprimir una lista con las categorias presentes en dpa_despar
---
Reparación de geometrias
---
Visualización de la capa LOTE y la capa ba003_uso_suelo_edificabilidad_a 
---
Inspección de la estructura de las capas
---
Exploración visual de capas
---
**Contexto para el filtrado de las capas a usar**

El **Plan de Uso y Gestión del Suelo** es un instrumento de planificación, ordenación y gestión del suelo que instrumentaliza políticas que permitan viabilizar los
planteamientos definidos en el PMDOT; que regula el uso y la edificabilidad del suelo urbano y rural; fue aprobado Ordenanza Metropolitana 044-2022 11 de noviembre 2022

*   Componente estructurante que clasifica el suelo en urbano y rural y su subcalsificacion, duracion de 12 años
*   Componente urbanistico define instrumentos de planeamiento del suelo tales como: Polígonos de Intervención Territorial, Tratamientos urbanísticos, Usos de suelo, Edificabilidad y Estándares urbanísticos.
*   Aplicacion de planes complementarios que permite detallar, completar y desarrollar de forma específica las determinaciones
*   Gestion del suelo a partir de instrumentos  de gestión y financiamiento urbano

Acorde a la descrpcion del contenido de las capas se identifica que las **capas a usar** para analizar el monitoreo del uso del suelo en la parroquia de San Antonio de Pichincha del Distrito Metropolitano de Quito son:

*   ba003_uso_suelo_edificabilidad_a
*   ba004_prevision_suelo_vivienda_interes_social_a
*   bd001_plan_urbanistico_complementario_a
*   bi001_declaratoria_regularizacion_prioritaria_a
*   LOTE
*   BLOQUE_CONSTRUCTIVO
*   UNIDAD_CONSTRUCTIVA
*   MANZANA
*   AIVAS
*   organizacion_territorial_parroquial_rural_a
---
Chequeo de datos nulos, no data, valores negativos
---
Filtrado de campos
---

3. Analisis exploratorio de los datos + Visualizacion de datos
---
ba003_uso_suelo_edificabilidad_a
---
ba004_prevision_suelo_vivienda_interes_social_a
---
bd001_plan_urbanistico_complementario_a
---
bi001_declaratoria_regularizacion_prioritaria_a
---
LOTE
---
BLOQUE_CONSTRUCTIVO
---
UNIDAD_CONSTRUCTIVA
---
MANZANA
---
AIVAS
