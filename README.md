# Inmigración a Canadá (1980-2013)

Este proyecto es un ejercicio práctico en dos etapas fundamentales: primero, la limpieza y estructuración de un conjunto de datos en bruto utilizando **Pandas**; y segundo, el análisis visual de tendencias y patrones migratorios clave utilizando **Matplotlib**. 

## 💾 Sobre los Datos

*   **Origen:** Datos oficiales de la Organización de las Naciones Unidas (ONU) sobre flujos migratorios internacionales.
*   **Dataset Original:** Archivo de Excel (`Canada.xlsx`) con el registro anual de inmigrantes de 195 países clasificados por su región geográfica y nivel de desarrollo.
*   **Dataset Procesado:** Archivo en formato CSV (`Canada.csv`) optimizado y limpio, listo para ser consumido por las librerías de graficación.

---

## 📌 Estructura del Proyecto (Flujo de Trabajo)

El proyecto está dividido en dos cuadernos de Jupyter (`.ipynb`) independientes pero conectados secuencialmente:

### Etapa 1: Preprocesamiento y Limpieza de Datos (`preprocesamiento_Pandas.ipynb`)
En esta primera fase, se abordan los desafíos típicos de la preparación de datos (*Data Cleaning*):
1.  **Carga y Exploración:** Importación del archivo Excel original omitiendo las filas informativas del inicio y del final. Inspección de la estructura técnica mediante `.head()`, `.tail()` e `.info()`.
2.  **Limpieza Profunda:** Eliminación de columnas irrelevantes (códigos internos de la ONU), tratamiento de valores nulos y renombrado de columnas complejas por nombres legibles (ej. `OdName` por `Country` o `AreaName` por `Continent`).
3.  **Enriquecimiento:** Creación automatizada de una columna 'Total' que suma todos los inmigrantes recibidos por cada país a lo largo de los 34 años de estudio.
4.  **Indexación y Consultas Avanzadas:** Configuración de los nombres de los países como el índice principal para permitir búsquedas y filtros rápidos mediante `.loc` e `.iloc` (ej. filtrado por condiciones o regiones específicas como "África Meridional").

### Etapa 2: Visualización de Datos y Análisis de Tendencias (`matplotlib.ipynb`)
Una vez obtenidos los datos limpios, se procede a la fase de análisis visual para extraer conocimiento:
1.  **Configuración del Entorno Visual:** Inicialización de `matplotlib.pyplot` y aplicación de estilos profesionales de presentación (como el estilo clásico `ggplot`).
2.  **Estudio de Caso (Haití):** Construcción de un gráfico de líneas continuo para analizar la evolución temporal. Se destaca el pico migratorio del año 2010 como consecuencia del catastrófico terremoto de magnitud 7.0, utilizando funciones de anotación de texto (`plt.text`) sobre el gráfico.
3.  **Análisis Comparativo (India vs. China):** Uso de la transposición de matrices (`.transpose()`) en Pandas para cruzar y comparar en un mismo gráfico de líneas la evolución de los dos países que históricamente más inmigrantes han aportado a Canadá.
4.  **Estudio de los 5 Países Principales:** Configuración de gráficos a gran escala (`figsize=(14, 8)`) para visualizar de manera simultánea y legible las curvas de las cinco mayores fuentes migratorias, ordenadas mediante `.sort_values()`.

---

## 🛠️ Tecnologías Utilizadas

*   **Python 3**
*   **Pandas:** Para la manipulación, limpieza, indexación y agregación de los dataframes.
*   **NumPy:** Para soporte de cálculos matemáticos y científicos.
*   **Matplotlib:** Para el diseño y personalización de las gráficas de líneas.
*   **Openpyxl:** Motor necesario para la lectura de los archivos originales de Excel.

## 🚀 ¿Cómo ejecutar el proyecto?

1.  Instala las dependencias necesarias en tu entorno de terminal:
    ```bash
    pip install pandas numpy matplotlib openpyxl
    ```
2.  **Paso 1 (Opcional):** Ejecuta `preprocesamiento_Pandas.ipynb` si deseas ver cómo se transformó el archivo original de Excel y cómo se estructuraron las consultas de datos.
3.  **Paso 2:** Ejecuta `matplotlib.ipynb` para cargar los datos limpios de la nube y generar todos los análisis visuales y las gráficas estadísticas del proyecto.
