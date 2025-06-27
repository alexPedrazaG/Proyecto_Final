# 🚀PROYECTO Final Python

## 📌 Descripción
En este proyecto debes demostrar los conocimientos que has adquirido a lo largo de todo el programa. Deberás realizarlo una vez hayas completado todo el contenido obligatorio del programa y hayas entregado y superado todos los proyectos previos. Objetivo del proyecto: En este proyecto tienes que enfrentarte al folio en blanco. Es un proyecto libre donde tú marcas el objetivo de tus análisis. El proyecto se tiene que centrar en un EDA y Dashboard de un conjunto de datos a tu elección.

## 🗂️ Estructura del Proyecto
├── anlisis Power BI # Proyecto_Final_EDA.pbix # Contiene el archivo de Power BI con todas las visualizaciones

├── anlisis Py # LimpiezaDatos_EDA_Python.py # Contiene el archivo de python con toda la programación

├── data # campaign_desc.csv, campaign_table.csv, causal_data.csv, coupon.csv, coupon_redempt.csv, hh_demographic.csv, product.csv y transaction_data.csv   # Son los ficheros de análisis descargados desde 'kaggle'

├── docs # Dunnhumby_Complete_Journey.doc y dunnhumby - The Complete Journey User Guide.pdf # Descripción del significado de los ficheros y desde donde se ha descargado

├── results # archivo_limpio_causal.csv, archivo_limpio_household.csv y archivo_limpio_product.csv # Resultado de los archivos después de haber hecho limpieza de datos y creación de nuevos campo

├── README.md # Descripción del proyecto

## 🛠️ Instalación y Requisitos
En este proyecto es necesario utilizar:

+ Python 3.13.2 (es la versión que he utilizado para hacer los ejercicios)
+ Librerias: Pandas, Numpy y Locale
+ Visual Studio Code
+ Power BI

## 🎯 Criterios
- Requisitos mínimos del conjunto de datos.
- Uso eficiente de Python y Pandas.
- Uso eficiente de una herramienta de visualización de datos.
- Transformación y limpieza de los datos.
- Análisis descriptivo de los datos.
- Análisis estadístico de los datos.
- Dashboard operativo de los datos.
- Informe explicativo del análisis.
- Readme del proyecto.
- Correcta organización del repositorio de Github

*Importante: Faltarían por añadir 3 ficheros en las carpetas correspondientes, que por volumetría no me deja subirlo. De todas formas lo adjuntaré en el .zip y esos ficheros son: causal_data.csv, transaction_data.csv y archivo_limpio_causal.csv*


## 📊 Análisis de proyecto
### 1. Introducción y Preparación de los Datos
Se ha llevado a cabo un Análisis Exploratorio de Datos (EDA) a partir del historial de compras durante dos años de un grupo de 2.500 hogares en un supermercado. Las fechas incluidas en el conjunto de datos se expresaban como un contador de días, por lo que se ha asumido que el día 0 corresponde al 01/01/2017, para poder traducir estos valores a un calendario real. En la fase inicial, se procedió a una limpieza exhaustiva de los datos dónde se han cambiado formatos, se han borrado campos que no eran necesarios, se han creado nuevos derivados de la información original, se ha filtrado el fichero, se han control de nulos...

De los siete ficheros originales disponibles, finalmente se trabajó con tres, seleccionados por su relevancia y volumen de datos. La decisión de reducir el número de ficheros también respondió a criterios de rendimiento, ya que la combinación de todos generaba archivos demasiado grandes para su tratamiento eficiente.

El análisis se ha llevado a cabo utilizando Power BI, herramienta con la cual se gestionaron los ficheros como tablas interrelacionadas. Se crearon dos tablas adicionales: una de medidas y otra correspondiente al calendario, permitiendo una correcta gestión temporal de las visualizaciones.

### 2. Diseño del Dashboard
El dashboard interactivo resultante se ha dividido en seis pestañas. En todas ellas se ha incorporado un marcador de filtro (imagen interactiva en la parte superior derecha), que al ser activado despliega una selección de filtros aplicables a toda la pestaña.

Además, el dashboard ha sido optimizado tanto para visualización en escritorio como para dispositivos móviles. En la versión móvil, los filtros se han reorganizado y colocados justo debajo del título para facilitar su uso.

### 3. Resumen General (General Summary)
El objetivo principal de esta pestaña es ofrecer una visión panorámica del rendimiento general de las ventas.

**Indicadores Clave (KPIs)**  
Se muestran 4 tarjetas con métricas agregadas:

- Ventas Totales: 346.981,45 €
- Total de Transacciones: 21.295
- Total de Tiendas: 153
- Total de Productos: 10.747

Estas métricas permiten comprender rápidamente el alcance y volumen de operaciones del supermercado.

**Gráficos y Visualizaciones**  
**1. Ventas por Tienda (Gráfico de barras)**  
Este gráfico permite identificar las tiendas más rentables. Destacan:

- Tienda 406: 22.381,2 €
- Tienda 367: 13.990,6 €
- Tienda 368: 10.657,9 €

Este análisis permite detectar puntos de venta con mejor desempeño y sirve como base para estrategias de expansión o refuerzo.

**2. Ventas por Semana (Gráfico lineal)**  
Se visualiza la evolución semanal de las ventas. Las semanas más destacadas son:

- Semana 92: 5.349,08 €
- Semana 63: 5.092,47 €
- Semana 61: 4.732,20 €

Este patrón puede ayudar a identificar estacionalidades o efectos de campañas específicas.

**3. Ventas por Tipo de Campaña (Gráfico circular)**  
Este gráfico muestra claramente la efectividad de las campañas promocionales:

- Campaña Tipo A: 328.570 € (claramente dominante)
- Campaña Tipo B: 17.320 €
- Campaña Tipo C: 1.100 €

El dominio de la campaña tipo A sugiere una oportunidad para replicar su enfoque en otras tiendas o períodos.

**Filtros Interactivos**  
Se han incluido cuatro segmentadores que permiten analizar los gráficos de manera personalizada:

- Tienda
- Año
- Semana
- Tipo de Campaña

Estos filtros facilitan el análisis dinámico según el criterio del usuario y favorecen una toma de decisiones más informada.

**Conclusiones del Resumen General**  
+ Existe una alta concentración de ventas en un pequeño número de tiendas, lo que puede indicar ubicaciones estratégicamente exitosas.
+ Las ventas semanales presentan picos significativos, que podrían estar asociados a campañas o eventos externos (festivos, promociones).
+ La campaña tipo A es claramente la más efectiva, representando la gran mayoría de las ventas, lo que justifica un análisis más profundo de sus características.

###  4. Análisis de Producto (Product Analysis)
El objetivo de esta pestaña es analizar el rendimiento de los productos a nivel individual, por departamento y por valor generado. Este análisis permite identificar qué artículos y categorías aportan mayor volumen de ventas, ya sea en cantidad de unidades o en términos monetarios.

**Gráficos y Visualizaciones**  
**1. Productos más vendidos (Gráfico de barras)**  
Este gráfico muestra los productos con mayor volumen de unidades vendidas. Permite detectar aquellos artículos con mayor rotación en el supermercado. Los productos destacados son:

- Producto 1082185: 3.396 unidades vendidas
- Producto 5582789: 2.405 unidades vendidas
- Producto 995242: 1.943 unidades vendidas

Esto es útil para identificar los productos de alta demanda, clave para una correcta gestión del inventario.

**2. Top 10 departamentos por ventas (Gráfico circular)**  
Este gráfico refleja qué departamentos generan el mayor ingreso total, lo cual ayuda a entender qué secciones del supermercado son más relevantes a nivel de facturación. Destacan:

- GROCERY con 137.898,50 €
- MEAT con 62.991,23 €
- PRODUCE con 60.839,21 €

Estos datos pueden orientar decisiones estratégicas en cuanto a promociones, distribución del espacio en tienda o enfoque comercial.

**3. Productos con Mayor Facturación (Gráfico de barras)**  
Aquí se analizan los productos que, aunque no necesariamente se venden en mayor cantidad, generan más ingresos totales. Esta métrica es clave para evaluar el impacto económico de cada producto en las ventas generales. Los productos con mayor recaudación son:

- Producto 916122: 3.527,44 €
- Producto 1082185: 3.282,45 €
- Producto 1029743: 2.717,41 €

Este enfoque ayuda a identificar productos con mayor margen o precio unitario alto.

**4. Tabla Resumen de Productos**  
Esta tabla complementaria ofrece una visión detallada por producto, agrupando la siguiente información:

- Departamento al que pertenece el producto
- Marca (nacional o privada)
- Cantidad total vendida (unidades)
- Total de ventas en euros
- Precio promedio por unidad

Esta tabla es especialmente útil para combinar información de cantidad y valor económico, permitiendo así detectar patrones relevantes por categoría o marca.

**Filtros Interactivos**  
Se han incluido cuatro segmentadores que permiten analizar los gráficos de manera personalizada:

- Tienda
- Año
- Semana
- Tipo de Campaña

Gracias a estos filtros, el usuario puede enfocar el análisis en períodos o tiendas concretas, o incluso evaluar el efecto de campañas específicas sobre el comportamiento de los productos.

**Conclusión del Análisis de Producto**  
+ Algunos productos tienen una alta rotación, lo que los convierte en piezas clave para mantener la fidelidad del cliente y asegurar disponibilidad constante.
+ Otros, en cambio, generan altos ingresos pese a venderse en menor cantidad, lo cual puede estar asociado a un mayor precio unitario o margen comercial.
+ A nivel de departamentos, los datos indican que “Grocery”, “Meat” y “Produce” son las áreas más rentables, por lo que deberían recibir especial atención en campañas de marketing y gestión de stock.

Esta información puede ser aprovechada para optimizar el surtido, negociar con proveedores o definir estrategias de promoción según el peso económico real de cada producto o categoría.

###  5. Precios y descuentos (Price & Discounts)
Esta sección tiene como objetivo analizar el impacto que tienen los precios, los descuentos promocionales y el uso de cupones en las ventas, con especial atención en cómo varían entre departamentos y cómo influyen en el comportamiento del consumidor.

**Gráficos y Visualizaciones**  
**1. Ahorro promedio por unidad y por departamento (Gráfico de barras apiladas)**  
Este gráfico compara tres valores clave:

- Precio promedio pagado por el cliente
- Precio promedio de estantería
- Ahorro promedio (diferencia entre ambos)

Los departamentos están ordenados de forma ascendente según el ahorro medio. Los departamentos donde los clientes han obtenido un mayor ahorro son:

- SEAFOOD-PCKGD: 2,86 € de ahorro medio por unidad
- SEAFOOD: 2,82 € de ahorro medio por unidad
- MEAT: 2,72 € de ahorro medio por unidad

Este análisis permite identificar los sectores donde las promociones han tenido mayor impacto directo en el precio final pagado por el cliente.

**2. Ventas vs. Precio Promedio por Departamento (Gráfico de dispersión con Tamaño por Cupones Usados)**  
Este gráfico bidimensional representa:

- Eje X: Precio promedio del departamento
- Eje Y: Ventas totales
- Tamaño de la burbuja: Recuento de cupones utilizados
- Color: Total de ventas (intensidad del color)

Se incluyen además notas informativas dentro del gráfico para facilitar su interpretación. Los departamentos más destacados son:

- GROCERY: 137.898,50 € en ventas | Precio medio: 1,56 € | 53.051 cupones usados
- MEAT: 62.991,23 € | Precio medio: 3,72 € | 9.862 cupones usados
- PRODUCE: 60.839,21 € | Precio medio: 1,69 € | 28.445 cupones usados

Este gráfico permite identificar qué departamentos combinan un precio competitivo con un alto volumen de ventas y una fuerte influencia de cupones.

**3. Descuento total minorista por departamento (Gráfico de barras)**  
Se visualiza el total de descuentos otorgados directamente por los minoristas, agrupado por departamento. Solo se muestran aquellos que han recibido descuentos, gracias a un filtro aplicado. Destacan:

- GROCERY: 36.277,11 €
- MEAT: 20.071,95 €
- MEAT-PCKGD: 8.690,37 €

Estos valores muestran dónde se concentra el esfuerzo promocional por parte de los comercios.

**4. Cupones coincidentes por departamento (Gráfico de barras)**  
Aquí se muestran los departamentos en los que se han aplicado cupones coincidentes (es decir, que coincidían con el producto comprado). Se ha filtrado el gráfico para mostrar solo departamentos con más de un cupón coincidente. Destacan:

- GROCERY: 774 cupones coincidentes
- DRUG GM: 82 cupones coincidentes
- MEAT-PCKGD: 80 cupones coincidentes

Esto refleja la intensidad promocional basada en cupones por categoría de producto.

**5. Ventas con y sin uso de cupones (Gráfico circular)**  
Este gráfico ilustra el peso de las ventas realizadas con cupones respecto al total:

- Ventas con cupón: 5.766,57 €
- Ventas sin cupón: 341.214,88 €

Aunque los cupones están presentes, su impacto en el total de las ventas es aún limitado.

**Filtros Interactivos**  
Se han incorporado cuatro segmentadores que permiten personalizar el análisis según diferentes dimensiones temporales y comerciales:

- Tienda
- Estación del año
- Semana
- Tipo de Campaña

Estos filtros permiten explorar cómo cambian los patrones de descuentos y ahorro dependiendo del momento o ubicación, mejorando la toma de decisiones.

**Conclusión del Análisis de Precios y Descuentos**  
+ Los descuentos han sido particularmente significativos en los departamentos SEAFOOD y MEAT, donde los clientes han conseguido el mayor ahorro promedio por unidad.
+ GROCERY es el departamento con mayor volumen de cupones utilizados y descuentos minoristas, lo que indica una estrategia promocional intensiva.
+ A pesar de la alta cantidad de cupones usados en algunos departamentos, la proporción de ventas realizadas con cupones sigue siendo baja en comparación con las ventas totales (menos del 2%).
+ El cruce entre precio promedio, ventas y uso de cupones (gráfico de dispersión) muestra que los productos con precios más bajos tienden a tener más ventas y mayor uso de cupones, lo que sugiere que las promociones tienen un mayor impacto en productos de consumo frecuente y bajo coste.

Este análisis puede ser útil para ajustar las estrategias de pricing y promociones, reforzar aquellas que son efectivas y reconsiderar el uso de cupones en categorías donde no se observa un retorno significativo.

###  6. Clientes y Demografía (Customers & Demographics)
Esta sección tiene como finalidad comprender cómo varía el comportamiento de compra entre diferentes tipos de hogares según su edad, nivel de ingresos y tamaño familiar. El análisis permite detectar patrones de consumo asociados a grupos demográficos específicos y evaluar su impacto en las ventas y el uso de cupones.

**Visualizaciones y Análisis**  
**1. Ventas totales por grupo de edad (Gráfico de barras)**  
Este gráfico permite visualizar el total de ventas generadas por cada grupo de edad. Los grupos con mayor participación en las ventas son:

- 45-54 años: 152.193,52 €
- 35-44 años: 90.156,27 €
- 25-34 años: 59.156,55 €

Esto sugiere que los hogares en edad media son los principales impulsores del consumo en el supermercado.

**2. Ventas totales por nivel de ingreso (Gráfico de barras)**  
Aquí se analiza el total de ventas según los ingresos del hogar. Se destacan:

- 50-74K: 109.961,59 €
- 35-49K: 51.801,13 €
- 75-99K: 49.602,61 €

Los hogares con ingresos medios representan el mayor volumen de ventas, lo cual es coherente con un perfil de consumidores habituales y estables.

**3. Ventas totales por tamaño de hogar (Gráfico de barras)**  
Este gráfico muestra cómo varía el consumo según el número de personas por hogar. Se observa que:

- Hogares de 2 personas: 132.100,56 €
- Hogares de 1 persona: 90.857,92 €
- Hogares de 3 personas: 53.301,35 €

Los hogares pequeños (1-2 miembros) concentran la mayor parte del consumo, lo que podría influir en decisiones sobre formatos de productos o promociones.

**4. Ventas y uso de cupones por nivel de ingreso y grupo de edad (Gráfico de dispersión)**  
Este gráfico hay un símbolo de información que muestra:

- Eje X: Nivel de ingresos
- Eje Y: Total de ventas
- Tamaño de burbuja: Cantidad de cupones usados
- Color: Grupo de edad

Algunos hallazgos clave:

- Grupo 45-54 años lidera en casi todos los niveles de ingreso, tanto en ventas como en uso de cupones.
- Los hogares con ingresos entre 50-74K tienen el mayor volumen de ventas y también un alto uso de cupones (14.113).
- Incluso en niveles de ingresos bajos (ej. under 15K), se observa un uso considerable de cupones, lo que sugiere una mayor sensibilidad al precio.

Este gráfico permite visualizar la interacción entre poder adquisitivo, edad y comportamiento promocional.

**5. Tabla Resumen Demográfica**  
La tabla final ofrece una vista detallada de cada combinación de grupo demográfico con las siguientes métricas:

- Grupo de edad
- Nivel de ingresos
- Tamaño del hogar
- Cantidad total vendida (unidades)
- Total de ventas en euros
- Porcentaje de cupones usados

Es una herramienta clave para realizar análisis comparativos y segmentar al cliente con mayor precisión.

**Filtros Interactivos**  
Para facilitar un análisis más detallado y personalizado, se han incorporado los siguientes segmentadores:

- Tienda
- Nivel de ingresos
- Semana
- Grupos de edad

Estos filtros permiten realizar cruces entre distintas dimensiones y entender cómo se comportan los distintos perfiles de clientes en contextos específicos.

**Conclusión del Análisis de Clientes y Demografía**  
+ Los clientes más activos en términos de ventas pertenecen principalmente al grupo de edad 45-54 años, lo que sugiere que es un perfil prioritario para estrategias de fidelización.
+ Los hogares con ingresos medios (50-74K) y tamaños pequeños (1-2 personas) generan la mayor parte de las ventas, por lo que las campañas y promociones podrían adaptarse mejor a este perfil.
+ El uso de cupones es significativo incluso en niveles bajos y medios de ingresos, lo que indica una alta receptividad a promociones en diversos segmentos económicos.
+ La combinación de edad e ingresos permite construir un perfil de consumidor frecuente: personas de mediana edad con ingresos medios, que valoran los descuentos y representan una base sólida para el negocio.

Este análisis demográfico es esencial para personalizar estrategias de marketing, mejorar la segmentación y optimizar las ofertas según las características reales de los clientes.


###  7. Análisis de Campañas (Analysis of Promotional Campaigns)
Esta sección busca evaluar la efectividad de las campañas promocionales, considerando el volumen de ventas, la cantidad de cupones canjeados y la estacionalidad. Se pretende identificar cuáles campañas y períodos del año han tenido mayor impacto comercial.

**Visualizaciones y Análisis**  
**1. Cupones coincidentes vs. Ventas estacionales (Gráfico de dispersión con tamaño por cantidad vendida)**  
Este gráfico hay un símbolo de información que muestra:

- Eje X: Recuento de cupones coincidentes
- Eje Y: Ventas totales
- Tamaño de burbuja: Cantidad total de unidades vendidas
- Color: Estación del año

Permite entender el impacto del uso de cupones según la temporada. Se destacan:

- Summer-18, es la estación más destacada, con una combinación óptima de alto número de cupones coincidentes, gran volumen de ventas y alta cantidad de productos vendidos. Esto indica que las campañas de verano fueron tanto bien planificadas como efectivas en su ejecución.
- Spring-18, también muestra una fuerte respuesta a los cupones, lo que sugiere que las campañas en esta temporada lograron activar eficazmente el comportamiento de compra a través de incentivos.
- Winter-18, presenta un menor número de cupones utilizados y un volumen de ventas más bajo, lo que podría deberse a una menor intensidad promocional o a una menor disposición del consumidor a responder a campañas durante esa estación.

Esto evidencia que las campañas en verano generaron mayor volumen de ventas y participación.

**2. Participación en campañas por estación (Gráfico de embudo)**  
Este gráfico muestra la cantidad de interacciones o participaciones en campañas por estación. Resultados clave:

- Summer-18: 47.832
- Spring-18: 36.840
- Winter-18: 21.014

Verano no solo lidera en ventas, sino también en participación, indicando una mayor receptividad del cliente en ese período.

**3. Campañas con más cupones canjeados (Gráfico de barras)**  
Se muestra el total de cupones canjeados agrupados por campaña. Destacan:

- Campaña 18: 46.402
- Campaña 13: 36.178
- Campaña 8: 20.643

Estas campañas no solo han logrado difusión, sino una alta conversión mediante cupones.

**4. Evolución de ventas por estación (Gráfico de líneas)**  
Muestra cómo variaron las ventas a lo largo de las estaciones del año. Se observa un crecimiento sostenido, con un claro pico en verano:

- Summer-18: 149.820,41 €
- Spring-18: 112.844,48 €
- Winter-18: 71.368,67 €

Esto refuerza la estacionalidad como factor clave en la estrategia promocional.

**5. Total de ventas por campaña (Gráfico de barras)**  
Representa la evolución del total de ventas alcanzadas por cada campaña. Sobresalen:

- Campaña 18: 145.363,53 €
- Campaña 13: 110.809,74 €
- Campaña 8: 69.236,19 €

Esto permite identificar cuáles campañas tuvieron mayor impacto financiero directo.

**Filtros Interactivos**  
Para una exploración más detallada y contextualizada, se han habilitado los siguientes segmentadores:

- Tienda
- Estación del año
- Semana
- Tipo de campaña

Estos filtros permiten analizar el rendimiento de las campañas según la ubicación y el momento del año, lo que facilita la toma de decisiones futuras.

**Conclusión del Análisis de Campañas**  

+ Summer-18 se consolida como la estación más efectiva en términos de ventas, participación y cantidad de unidades vendidas, lo que indica un alto grado de efectividad de las campañas lanzadas durante ese período.
+ Las campañas numeradas 18, 13 y 8 son las más exitosas tanto en volumen de cupones canjeados como en ventas generadas.
+ Existe una correlación positiva entre campañas con alto canje de cupones y un mayor volumen de ventas, lo que valida la efectividad del uso de cupones como herramienta promocional.
+ La estacionalidad juega un rol importante: las campañas lanzadas en primavera y verano han generado mejores resultados que las realizadas en invierno.

Este análisis puede utilizarse como base para diseñar futuras campañas, priorizando temporadas de alto impacto y reforzando el uso de cupones en períodos de mayor receptividad del cliente.

###  8. Análisis temporal (Temporal Analysis)
Esta sección tiene como propósito identificar patrones de comportamiento en el tiempo, analizando cómo varían las ventas y las transacciones a lo largo de los días de la semana y del mes. Esta información es clave para optimizar decisiones operativas como la gestión de personal, promociones específicas o reposición de stock.

**Visualizaciones y Análisis**  
**1. Distribución de ventas por día de la semana (Mapa de calor)**  
El análisis revela que los días con mayor volumen de ventas son:

- Viernes: 67.988,20 €
- Jueves: 62.442,82 €
- Sábado: 46.807,12 €

Esto refleja una clara tendencia a realizar compras hacia el final de la semana, posiblemente relacionadas con la preparación del fin de semana o promociones activas en esos días.

**2. Análisis de estacionalidad por mes y día de la semana (Gráfico de columnas apiladas)**  
Este gráfico hay un símbolo de información que muestra:

- Eje X: Día del mes
- Eje Y: Ventas totales
- Leyenda: Día de la semana

Se observa que los siguientes días del mes concentran un mayor volumen de ventas: 

- 15: 3.833,43 € (jueves)
- 23: 3.162,47 € (viernes)
- 1: 3.127,72 € (jueves)

En todos los casos, estas fechas coinciden con días de semana de alta actividad, como jueves y viernes, lo que sugiere un patrón mensual que refuerza los picos semanales.

**3. Frecuencia de transacciones según el día de la semana (Gráfico de barras)**  
Los siguientes días de la semana son dónde mayor número de transacciones se producen: 

- Viernes: 3.713 
- Jueves: 3.448 
- Sábado: 3.086 

Esta alineación con el comportamiento de ventas indica que los picos no se deben a compras más grandes, sino a una mayor afluencia de clientes esos días.

**4. Distribución de ventas por día del mes (Gráfico de dispersión)**  
Este gráfico hay un símbolo de información que muestra:

- Eje X: Ventas totales
- Eje Y: Día del mes
- Tamaño de burbuja: Ventas totales

Ciertos días del mes presentan ventas totales significativamente más altas, destacando los días:

- Día 14: 13.768,63 €
- Día 3: 13.102,31 €
- Día 15: 12.778,83 €

Estos días podrían coincidir con momentos clave del ciclo económico de los hogares (inicio, mediados y segunda semana del mes), donde tiende a haber mayor liquidez o acciones promocionales.

**5. Evolución por día del mes por el promedio de ventas y cupones usados (Gráfico de líneas)**  
Los mismos días con mayor venta también registran un uso elevado de cupones:

- Día 3: 4.345 
- Día 14: 4.295
- Día 15: 4.020 

Esto sugiere que las promociones son más efectivas cuando se lanzan en días de alto flujo natural, amplificando su impacto comercial.

**Filtros Interactivos**  
Se incluyen cuatro segmentadores que permiten analizar los gráficos de forma dinámica según diferentes ejes temporales y comerciales:

- Tienda
- Estación del año
- Semana
- Tipo de campaña

Estos filtros aportan flexibilidad al análisis, permitiendo estudiar picos de actividad según contexto o temporada.

**Conclusión del Análisis de Campañas**  
+ Las ventas y transacciones se concentran principalmente entre jueves y viernes, lo que convierte estos días en puntos estratégicos para campañas y gestión operativa.
+ Existen días del mes con picos sistemáticos de consumo, como el 3, 14 y 15, que coinciden con alto uso de cupones y podrían estar vinculados a calendarios salariales o hábitos de gasto.
+ El uso de cupones tiende a coincidir con los días de mayor venta, lo que refuerza su eficacia como herramienta promocional si se aplica en los momentos adecuados.
+ Este análisis temporal es clave para la planificación de promociones, refuerzo de personal y diseño de ofertas específicas, maximizando el rendimiento en los días de mayor impacto comercial.

## 🧠 Conclusión
1. Replicar el modelo de éxito en tiendas líderes:
Identificar qué factores hacen que tiendas como la 406 tengan un desempeño superior (ubicación, surtido, gestión) y escalar estas prácticas al resto de puntos de venta.

2. Optimizar surtido según rentabilidad:
Reforzar productos con alta rotación y alto margen, revisando el espacio en tienda, el stock disponible y las acciones promocionales en torno a ellos.

3. Rediseñar la estrategia de cupones:
Aumentar el uso de cupones donde ya son efectivos (productos de consumo frecuente y bajo precio), pero revisar o eliminar cupones en categorías con bajo impacto, optimizando el gasto promocional.

4. Segmentar campañas por perfil demográfico:
Enfocar los esfuerzos de marketing en clientes de 45-54 años con ingresos medios, diseñando promociones y productos que encajen con sus hábitos de compra.

5. Aprovechar la estacionalidad y días pico:
Planificar acciones comerciales clave alrededor del verano y en los días del mes con mayor volumen (3, 14, 15). Esto incluye promociones, refuerzo de personal, campañas de fidelización y push en canales digitales.

6. Explorar nuevas oportunidades en campañas tipo B y C:
Dado que la campaña Tipo A domina, analizar las razones detrás del bajo rendimiento de los otros tipos y considerar rediseñarlas o sustituirlas.

7. Mayor análisis predictivo:
Aprovechar estos patrones temporales y demográficos para implementar modelos de predicción de demanda y así mejorar la planificación de stock y operaciones.
   
## 🤝 Contribuciones
Las contribuciones son bienvenidas. Si deseas mejorar el proyecto, por favor abre un pull request o una issue.

## ✒️ Autores

Alejandro Pedraza

@alexPedrazaG
