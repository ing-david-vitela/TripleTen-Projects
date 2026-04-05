# Análisis de Telecomunicaciones ConnectaTel 📱

## 🎯 Objetivo del Proyecto
El objetivo principal de este proyecto es analizar el comportamiento de uso de los clientes de ConnectaTel, una empresa de telecomunicaciones con operaciones en México y Colombia. A través de la exploración, limpieza y segmentación de datos, buscamos identificar patrones de consumo (llamadas y mensajes) para optimizar la oferta comercial, detectar comportamientos atípicos (Heavy Users) y proponer estrategias de retención y up-selling basadas en datos.

## 📂 Datasets Utilizados
El análisis integra tres bases de datos fundamentales:
- `users_latam.csv`: Información demográfica y contractual de clientes (edad, ciudad, plan contratado).
- `plans.csv`: Catálogo de los planes actuales (Básico y Premium) con sus beneficios y costos.
- `usage.csv`: Registro de la actividad real (duración de llamadas y longitud de mensajes de texto).

## 🛠️ Etapas del Análisis
1. **Carga y Exploración:** Revisión de la estructura inicial de los 3 datasets.
2. **Identificación de Calidad:** Detección de sentinels (valores imposibles como edades de -999 y ciudades "?") y fechas futuras.
3. **Limpieza de Datos:** Corrección de sentinels, imputación de nulos y verificación de nulos estructurales MAR (Missing At Random) según el tipo de evento (texto vs llamada).
4. **Summary Statistics:** Creación de un perfil de uso unificado agrupando consumo total por `user_id`.
5. **Visualización y Outliers:** Histogramas de consumo y segmentación demográfica. Identificación de Heavy Users mediante el método de Rango Intercuartílico (IQR).
6. **Segmentación:** Clasificación de clientes en grupos de uso ("Alto", "Medio", "Bajo") y grupos etarios.
7. **Insights Ejecutivos:** Traducción técnica a estrategias comerciales accionables (campañas de up-selling y reestructuración de planes para jóvenes).

## 🚀 Cómo ejecutar el proyecto (Guía de reproducción)
Para revisar y ejecutar este análisis de forma interactiva:
1. Descarga el archivo `.ipynb` de este repositorio.
2. Sube el notebook a **Google Colab** (o ábrelo en tu entorno local de Jupyter).
3. Asegúrate de tener las librerías necesarias instaladas (`pandas`, `matplotlib`, `seaborn`).
4. (Importante) Deberás cargar los 3 archivos CSV originales en el entorno de ejecución para que las celdas de carga funcionen correctamente.
5. Ejecuta las celdas en orden secuencial (Run All) desde la parte superior hasta el Insight Ejecutivo.
