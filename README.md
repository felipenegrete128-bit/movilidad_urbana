# 🧾 Resumen ejecutivo 

**Contexto & objetivo:**  
- Responde la pregunta central del análisis: ¿qué relación existe entre la movilidad urbana (congestión, tiempos de viaje) y la productividad económica (PIB per cápita)?
- México y Sao Paulo muestran mayores retrasos y también un PIB per cápita eledo, sin embargo, al ver el caso de Montevideo con un alto PIB pero baja incidencia en retrasos podemos inferir que la congestión no determina automáticamente la productividad; otros factores median esta relación. 

**Cobertura de datos:**  
- Especifica los años analizados, número de ciudades y países incluidos.
- Para este análisis se tuvo un enfoque específico al año 2024, del cual pudimos obtener datos de países latinoamericanos, de los cuales se obtuvo un total de 15   ciudades de 7 países diferentes. 

**Metodología (alto nivel):**  
- Describe los procesos principales: limpieza de datos (formatos, estandarización de columnas).
- Explica la agregación por ciudad–año y el uso de una unión INNER para integrar tráfico y economía.
- Menciona las validaciones visuales empleadas (distribuciones, outliers, tendencias generales).

La metodología aplicada se basó, en primer lugar, en explorar la estructura de los DataFrames para identificar los ajustes necesarios en el proceso de limpieza. Durante esta etapa se detectaron variables numéricas registradas como tipo objeto, así como caracteres especiales como ., , y % que fueron eliminados para garantizar un análisis correcto. Adicionalmente, se estandarizaron los nombres de las columnas de cada DataFrame.

Posteriormente, los datos fueron agrupados por ciudad, país y año, lo que permitió obtener una visión inicial del comportamiento entre tráfico y economía. A continuación, se realizó la unión de ambos DataFrames mediante un Inner Join, utilizando ciudad y año como claves de cruce.

Finalmente, se llevó a cabo una validación visual a través de tres tipos de gráficos: un gráfico de cajas para analizar los retrasos de tráfico (jams_delay), donde se identificaron valores atípicos (outliers) que sugieren posibles errores de medición; un histograma para analizar la distribución del PIB per cápita, evidenciando que la mayoría de ciudades se concentran entre 0.5 y 1.8; y un gráfico de barras para comparar la congestión vehicular con el PIB por ciudad.  


**Hallazgos iniciales:** 
- Resume los patrones más importantes entre índices de tráfico y PIB per cápita.
- Destaca anomalías u outliers que podrían requerir revisión adicional o un análisis más profundo.
  
Dentro de los principales hallazagos tenemos los siguiente:
- Montevideo tiene un PIB de 2.7 Millones (USD)  y jams_delay de 0.1 Miles (Min). Siendo la ciudad con mayor PIB.
- Mexico city tiene un PIB de 2.1 Millones (USD) y jams_delay de 2.8 Miles (Min). Siendo la ciudad con mayor jams_delay, importante esta información de jayms_delay, ya que se aleja mucho de las demás ciudades.
- Sao Paulo tiene un PIB de 1.5 Millones (USD) y jams_delay de 1.6 Miles (Min). Siendo la segunda ciudad con mayor jams_delay.
- Belo horizonte, Buenos Aires y Río de Janeiro tienen un jams_delay moderado, pero un PIB considerablemente medianamente alto entre 1 y 1.8.
De acuerdo con estos hallazgos podemos inferir que no hay una estrecha relación entre ambas métricas.

**Recomendaciones**  
Aterriza los hallazgos en acciones: ciudades prioritarias, necesidad de validar fuentes, requerimiento de análisis adicionales, o propuestas de inversión.

- ¿Qué ciudad : Bogotá, Lima o Buenos Aires o alguna otra en particular, muestra la mayor correlación significativa entre altos niveles de congestión vehicular y bajos indicadores de productividad económica, sugiriendo ser una ciudad prioritaria para inversión en infraestructura de transporte?

De acuerdo con la evidencia obtenida, Santiago seria una ciudad en la que seria ideal priorizar la inversión, ya que en ella si se logra identificar una relación proporcional entre congestión vehícular y bajos indicadores de productividad. La cual tiene un jams_delay de 0.6 miles (min) y un PIB de 0.2 Millones (USD)
