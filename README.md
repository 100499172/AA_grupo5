# Práctica 1 – Aprendizaje Automático  
**Curso:** 2024–2025  
**Asignatura:** Aprendizaje Automático  
**Trabajo práctico grupal**  
**Grupo:** 05  
**Integrantes:**  
- Elena Recio Álvarez – NIA: 100495725  
- Alejandra Castuera García – NIA: 100499172  

## Archivos entregados

Se incluyen los siguientes archivos en la entrega:

- `modelo_entrenamiento_FINAL_con_SMOTE.ipynb`: notebook principal que contiene el análisis exploratorio, evaluación de modelos, ajuste de hiperparámetros, tareas adicionales y conclusiones.
- `modelo_final.ipynb`: notebook que entrena el modelo final con todos los datos y genera las predicciones para el conjunto de competición.
- `modelo_final.pkl`: modelo final entrenado, guardado para su posterior reutilización.
- `predicciones.csv`: predicciones generadas para el conjunto de competición.

## Datos utilizados

Siguiendo las instrucciones del enunciado, se han utilizado los archivos correspondientes al grupo **07**, obtenidos sumando los dos últimos dígitos del NIA: 2 + 5 = 7.

Archivos utilizados:

- `attrition_availabledata_07.csv.gz` – Conjunto de entrenamiento y evaluación.
- `attrition_competition_07.csv.gz` – Conjunto sin etiquetas utilizado para la generación de predicciones.

## Estructura de la práctica

### Notebook 1: modelo_entrenamiento.ipynb

- Análisis exploratorio de los datos (EDA).
- Detección de valores nulos, columnas constantes y variables categóricas.
- Evaluación externa con partición holdout (2/3 train – 1/3 test).
- Evaluación interna mediante validación cruzada estratificada (StratifiedKFold).
- Evaluación de modelos básicos: KNN y Árboles de decisión, con ajuste de hiperparámetros.
- Evaluación de modelos avanzados: Regresión logística (con y sin L1) y SVM.
- Selección del mejor modelo.
- Tarea adicional:
  - Selección de atributos con `SelectKBest`
  - Aplicación de SMOTE como técnica de sobremuestreo para tratar el desbalanceo de clases
- Comparación y análisis de resultados en cada etapa.

### Notebook 2: modelo_final.ipynb

- Entrenamiento del modelo final utilizando todos los datos disponibles.
- Guardado del modelo en formato `.pkl`.
- Carga del conjunto de competición.
- Generación de predicciones.
- Exportación de las predicciones en formato `.csv`.

## Uso de herramientas de inteligencia artificial

Durante el desarrollo de esta práctica se ha hecho un uso limitado de herramientas de inteligencia artificial para:

- Resolver dudas puntuales relacionadas con funciones específicas de Python y bibliotecas como `scikit-learn`.
- Verificar estructuras de código y comprobar la correcta configuración de pipelines.
- Revisar explicaciones y redactar algunos comentarios para facilitar la comprensión.

Todo el contenido del trabajo ha sido revisado y comprendido por las autoras antes de su entrega.


