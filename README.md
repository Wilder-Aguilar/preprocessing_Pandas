# 📊 Preprocesamiento de Datos de Inmigración con Pandas

Este proyecto es un ejercicio práctico de análisis de datos con **Python** y **Pandas** para limpiar, filtrar y organizar un conjunto de datos sobre la inmigración en Canadá entre los años 1980 y 2013.

El objetivo principal es preparar y estructurar la información de manera limpia antes de realizar cualquier gráfico o visualización de datos.

---

## 💾 Sobre los Datos

* **Origen:** Datos oficiales de la Organización de las Naciones Unidas (ONU) sobre flujos migratorios internacionales.
* **Dataset original:** Archivo de Excel con el registro anual de inmigrantes de 195 países clasificados por su región geográfica y nivel de desarrollo.
* **Enlace de descarga:** [Descargar Canada.xlsx aquí](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DV0101EN-SkillsNetwork/Data%20Files/Canada.xlsx).

---

## 📌 ¿Qué hace este Notebook? (Paso a Paso)

El análisis del archivo `preprocesamiento_Pandas.ipynb` está dividido en tres etapas clave:

### 1. 📂 Carga y Exploración
* Importa el archivo de Excel omitiendo las filas de texto innecesarias del inicio y del final.
* Revisa las primeras y últimas filas (`.head()` y `.tail()`) y muestra un resumen técnico del contenido del DataFrame.

### 2. 🧹 Limpieza de Datos (Data Cleaning)
* Elimina columnas irrelevantes que no aportan valor al análisis (como códigos internos).
* Renombra columnas para que sean más fáciles de entender (por ejemplo, cambia `OdName` por `Country` e `AreaName` por `Continent`).
* Crea una columna 'Total' que suma de forma automática todos los inmigrantes de cada país a lo largo de los años estudiados.
* Verifica que no existan datos vacíos o nulos en el archivo.

### 3. 🔍 Consultas, Filtros y Ordenación
* Configura los nombres de los países como el índice principal (`index`) para poder buscar datos de forma rápida.
* Enseña a filtrar datos de países específicos (como Japón o Haití) usando búsquedas avanzadas con `.loc` e `.iloc`.
* Filtra la lista por múltiples condiciones (por ejemplo, ver solo países de la región de "África Meridional").
* Ordena los datos con `.sort_values()` para descubrir de manera automática cuáles fueron los países que más inmigrantes aportaron a Canadá.

---

## 🚀 ¿Cómo usar este proyecto?

1. Descarga el archivo `preprocesamiento_Pandas.ipynb` a tu computadora.
2. Ábrelo en tu entorno favorito de desarrollo (como Google Colab, Jupyter Notebook o VS Code).
3. Ejecuta cada celda de código en orden para ver cómo se transforman los datos paso a paso.
