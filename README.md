<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/3/33/F1.svg" alt="F1 Logo" height="80" align="middle">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/R_logo.svg" alt="R Logo" height="80" align="middle">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://upload.wikimedia.org/wikipedia/commons/d/d0/RStudio_logo_flat.svg" alt="RStudio Logo" height="80" align="middle">
</div>

<br>

# Análisis Exploratorio de Datos: Fórmula 1

<a href="https://www.r-project.org/"><img src="https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white" height="24"></a>
<a href="https://www.tidyverse.org/"><img src="https://img.shields.io/badge/Tidyverse-1A1A1A?style=for-the-badge&logo=R&logoColor=white" height="24"></a>
<img src="https://img.shields.io/badge/Status-Completado-success?style=for-the-badge" height="24">

El presente repositorio contiene un **Análisis Exploratorio de Datos (AED)** sobre estadísticas de carreras de la Fórmula 1, desarrollado como proyecto integrador para la asignatura *Laboratorio de Datos 1*. 

El objetivo principal de este trabajo es aplicar metodologías estadísticas de análisis univariado y bivariado, así como también técnicas de limpieza y transformación de datos relacionales.

---

## Tecnologías y Librerías

El análisis fue desarrollado en lenguaje **R**, utilizando principalmente el ecosistema **Tidyverse** para el procesamiento de los datos:

- `dplyr` y `tidyr`: Empleados para la manipulación estructural, uniones de tablas (joins), filtrado y creación de nuevas variables.
- `ggplot2`: Utilizado para el diseño y construcción de visualizaciones estadísticas.
- `janitor`: Implementado para la estandarización y limpieza de los nombres de variables.

## Estructura del Repositorio

La organización de los archivos en el repositorio es la siguiente:

- `data/`: Directorio que almacena los conjuntos de datos originales (`carreras.csv`, `conductores.csv`, `constructores.csv`, `resultados.csv`).
- `analisis_f1.Rmd`: Archivo fuente en R Markdown. Contiene la totalidad del código fuente, el proceso de limpieza y el análisis estadístico detallado.
- `analisis_f1.pdf`: **Reporte final compilado** listo para leer, con todos los resultados y gráficos del análisis.
- `README.md`: Documentación principal del proyecto.

## Alcance del Análisis

El documento `analisis_f1.Rmd` se estructura en las siguientes fases metodológicas:

1. **Importación y Limpieza**: Integración de cuatro bases de datos distintas mediante funciones `left_join` para consolidar un único conjunto de datos maestro.
2. **Transformación**: Tratamiento de valores nulos, filtrado de registros atípicos y conversión de unidades (transformación de milisegundos a minutos).
3. **Análisis Univariado**: Estudio de la distribución individual de variables clave, incluyendo estadísticos descriptivos y representaciones gráficas (histogramas y gráficos de barras).
4. **Análisis Bivariado**: Evaluación de la relación entre múltiples variables. Algunas de las cuestiones analizadas incluyen:
   - Impacto de las precipitaciones en la duración total de la carrera.
   - Variación en la tasa de abandonos frente a condiciones climáticas adversas.
   - Correlación lineal entre la posición inicial (grilla de largada) y la posición final obtenida.

## Instrucciones de Ejecución

Para replicar o revisar el análisis en un entorno local, siga estos pasos:

1. Clonar el repositorio en su equipo local:
   ```bash
   git clone https://github.com/lfmen/aedformula1.git
   ```
2. Abrir el archivo `analisis_f1.Rmd` utilizando **RStudio**.
3. Asegurarse de tener instalados los paquetes necesarios ejecutando:
   ```R
   install.packages(c("tidyverse", "janitor", "readxl"))
   ```
4. Ejecutar el código o generar el reporte final utilizando la herramienta **Knit** de RStudio.

---
*Proyecto desarrollado por Luca Franco Mengarelli.*
