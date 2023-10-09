# Proyecto: Relación entre la Producción Agropecuaria/Pesquera y la Generación de Empleos


Según Antonio Astiazarán Gutiérrez, el alcalde de Hermosillo, de acuerdo con la Encuesta Nacional de Ocupación y Empleo del INEGI, Hermosillo se encuentra entre los tres municipios más activos económicamente en el país, al nivel de Querétaro y Monterrey. Además, en 2023, Hermosillo experimenta su mayor actividad económica y creación de empleo en los últimos 25 años. Durante el período de enero a mayo de este año, se han generado 13 mil nuevos empleos formales en la ciudad. También resalta que el 54 por ciento de todos los empleos generados en Sonora provienen de Hermosillo. Asimismo, señala que la industria aeroespacial, automotriz, tecnológica y agrícola han experimentado un crecimiento significativo en la región.

Dado este contexto, se optó por llevar a cabo un análisis que permitiera examinar la creación de empleo en el sector agropecuario y pesquero como resultado de la producción en dichas áreas. En términos generales, el objetivo es analizar variables en estos campos en relación con los datos del IMSS, con el propósito de contar una historia basada en los datos que pueda respaldar la toma de decisiones de inversión en sectores que lo requieran y que puedan contribuir al crecimiento de la industria y la generación de empleo.


## 1. Objetivo del proyecto

El objetivo central de este proyecto es explorar la relación existente entre la producción agropecuaria y pesquera y la generación de empleos. En particular, buscamos identificar qué tipo de producción tiene un mayor impacto en la generación de empleos y entender cómo interactúan estos dos aspectos.

## 2. Fuentes de Datos y Variables

Para llevar a cabo este análisis, utilizaremos dos fuentes de datos principales: SAGARHPA (Secretaría de Agricultura, Ganadería, Desarrollo Rural, Pesca y Alimentación) e IMSS (Instituto Mexicano del Seguro Social).

Las variables que se considerarán incluyen, entre otras:
- Tipo de producción agropecuaria/pesquera.
- Valor producido
- Características de los asegurados.
- Áreas de actividad económica de los asegurados.

Fuentes principales de datos:
- [SAGARHPA: Agricultura](https://datos.sonora.gob.mx/conjuntos-de-datos/mostrar/datos-de-agricultura-sonora/1573)
- [SAGARHPA: Ganadería](https://datos.sonora.gob.mx/conjuntos-de-datos/mostrar/datos-ganaderia-sonora/1581)
- [SAGARHPA: Pesca](https://datos.sonora.gob.mx/conjuntos-de-datos/mostrar/datos-pesca-sonora/1582)
- [IMSS: Asegurados](http://datos.imss.gob.mx/dataset/asg2023/resource/asg-2023-01-31)

## 3. Limpieza y Preparación de Datos

En este proyecto, hemos llevado a cabo una serie de acciones cruciales en el proceso de limpieza y preparación de datos. Estas acciones incluyeron:

- **Selección de Características:** Identificamos y seleccionamos las características más relevantes para nuestros objetivos de análisis.

- **Identificación y Tratamiento de Valores Nulos:** Detectamos y manejamos los valores nulos de manera apropiada, ya sea llenándolos con datos válidos, eliminando las filas correspondientes o aplicando estrategias específicas según el contexto.

- **Estandarización de Formatos y Unidades:** Garantizamos que todas las columnas de datos tuvieran formatos y unidades coherentes para asegurar la consistencia en nuestro análisis.

- **Eliminación de Duplicados:** En caso necesario, eliminamos duplicados de los datos para evitar distorsiones en nuestras conclusiones y resultados.

- **Adecuación al Tipo de Dato:** Aseguramos que cada columna estuviera configurada con el tipo de dato adecuado para su contenido, lo que contribuyó a un análisis más preciso.

Estas acciones son fundamentales para garantizar que los datos estén limpios, coherentes y listos para su análisis.


## 4. Tablas "Tidy" Seleccionadas

Con el fin de llevar a cabo un análisis efectivo, hemos organizado los datos en tablas "tidy" que facilitan su manipulación y visualización. Estas tablas contienen información esencial relacionada con la producción y la generación de empleos.

1) **tidy_agricultura_ganaderia_pesca**: Hemos generado la tabla "tidy_agricultura_ganaderia_pesca.csv" que resume información detallada de SAGARHPA (Secretaría de Agricultura, Ganadería, Desarrollo Rural, Pesca y Alimentación). Esta tabla incluye las siguientes columnas:

- **ANO**: Año de producción.
- **SECTOR**: Sector de producción (agricultura, ganadería, pesca).
- **CVE_DDR**: Clave de la Delegación de Desarrollo Rural.
- **CVE_MUN**: Clave del Municipio.
- **ESPECIE_CULTIVO**: Especie o variedad de cultivo.
- **TIPO**: Tipo de producción (puede incluir información adicional sobre el tipo de cultivo o producción).
- **PRODTON**: Valor producido en toneladas.
- **VALPROD**: Valor producido en pesos.

Esta tabla proporciona una visión completa de la producción agropecuaria y pesquera, incluyendo datos específicos sobre los tipos de productos, especies, valores de producción y ubicaciones relacionadas con cada entrada.

2) **tidy_imss:** Hemos generado la tabla "tidy_imss.csv" que incluye las siguientes columnas:

- **rango_salarial**: Rango salarial de los empleados.
- **asegurados**: Cantidad de empleados asegurados.
- **no_trabajadores**: Número de trabajadores.
- **año**: Año de los datos.
- **mes**: Mes de los datos.
- **fecha**: Fecha de los datos.
- **municipio**: Municipio correspondiente.
- **sector_economico_1**: Sector económico nivel 1.
- **sector_economico_2**: Sector económico nivel 2.
- **sector_economico_4**: Sector económico nivel 4.
- **tamaño_patronal**: Tamaño de la patronal.
- **sexo**: Género de los empleados.
- **rango_edad**: Rango de edad de los empleados.
- **rango_salarial_descripcion**: Descripción del rango salarial.

Esta tabla contiene información detallada sobre el empleo, incluyendo datos relacionados con el salario, la cantidad de trabajadores, la ubicación geográfica y otros atributos relevantes.

## 5. Justificación

La relevancia de este análisis radica en la comprensión de cómo la producción agropecuaria y pesquera contribuye a la generación de empleos en la economía. Esta información puede ser valiosa para la toma de decisiones tanto a nivel gubernamental como en el sector privado, permitiendo una mejor planificación y asignación de recursos.

Estamos comprometidos a llevar a cabo un análisis riguroso y transparente, utilizando datos confiables y aplicando las mejores prácticas en el manejo de datos.


## 6. Información del contenido en el repositorio

1) **get_data.ipynb:** Esta libreta incluye el proceso de descarga de los datos de las fuentes. Se realizó un web scrapping para obtener los enlaces de descarga de todos los archivos históricos. Se seleccionaron características y se juntaron en un solo archivo por origen de datos. De tal manera que se generan 4 archivos csv correspondientes a los datos, y una serie de archivos correspondiente a los catálogos:

Datos principales:

  - **df_agricultura.csv**: Información histórica desde 2018-2023 de producción agrícola del estado de Sonora. 

  - **df_ganaderia.csv**: Información histórica desde 2018-2023 de producción pecuaria del estado de Sonora.

  - **df_pesca.csv**: Información histórica desde 2018-2023 de producción pesquera del estado de Sonora.

  - **df_imss.csv**: Información histórica desde 2018-2023 de asegurados por el IMSS en el estado de Sonora.

Catálogos de datos:

  - **cat_agricultura.xlsx**: Contiene un catálogo en cada pestaña con la codificación que se utiliza en la base de datos de agricultura de SAGARHPA. Estos catálogos se utilizaron dentro del procesamiento de datos para generar las tablas tidy.

  - **cat_ganaderia.xlsx**: Contiene un catálogo en cada pestaña con la codificación que se utiliza en la base de datos de ganaderia de SAGARHPA. Estos catálogos se utilizaron dentro del procesamiento de datos para generar las tablas tidy.

  - **cat_agricultura.xlsx**: Contiene un catálogo en cada pestaña con la codificación que se utiliza en la base de datos de pesca de SAGARHPA. Estos catálogos se utilizaron dentro del procesamiento de datos para generar las tablas tidy.
  
  - **imss_delegación-subdelegación.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar delegaciones y subdelegaciones.
  
  - **imss_entidad-municipio.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar entidades y municipios.
  
  - **imss_Layout.csv**: Diccionario original de la base de datos del IMSS (raw data).
  
  - **imss_Rango_edad.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar los rangos de edades.
  
  - **imss_Rango_salario.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar los rangos de salario de acuerdo al salario mínimo.

  - **imss_Rango_UMA.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar los rangos de salario de acuerdo a las UMAs.

  - **imss_sector_1.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar los sector (nivel 1) al que pertenece el registro.

  - **imss_sector_2.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar los sector (nivel 2) al que pertenece el registro.

  - **imss_sector_4.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar los sector (nivel 4) al que pertenece el registro.

  - **imss_sexo.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar el sexo.
  
  - **imss_Tamaño_de_registro_patronal.csv**: Catálogo con las claves que se utilizan en la base de datos del IMSS para codificar el rango de tamaño patronal.

Todos estos archivos se guardaron en la carpeta data.

2) **processing_data.ipynb:**  El proceso de selección de las variables o columnas con las que trabajaremos, así como los criterios de procesamiento y limpieza, se detallan en nuestra libreta [jupyter](https://github.com/anmerino-pnd/Proyecto_Trabajos_Generados/blob/main/processing_data.ipynb). Esta libreta genera las dos tablas tidy de nuestro proyecto (*tidy_agricultura_ganaderia_pesca*, y *tidy_imss*).


## 7. Referencias 

* Sonora, R. (2023, June 9). Hermosillo se encuentra dentro de los primeros municipios con mayor actividad económica del país: INEGI. Radio Sonora; Radio Sonora. https://radiosonora.com.mx/2023/06/09/hermosillo-se-encuentra-dentro-de-los-primeros-municipios-con-mayor-actividad-economica-del-pais-inegi/
