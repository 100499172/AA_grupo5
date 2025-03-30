## Estado del proyecto

Los **pasos 2 y 3** (EDA y configuración de la evaluación) ya estaban realizados desde la semana pasada.  
Simplemente **no los subimos aún a GitHub** porque no sabíamos que había que subir los notebooks.

Esta semana estamos trabajando en los **pasos 4 y 5**:
- Paso 4: Modelos básicos (KNN y Árboles de decisión)
- Paso 5: Modelos avanzados (Regresión logística y SVM)



# README – Trabajo de Aprendizaje Automático

Este repositorio contiene el desarrollo de los pasos 2, 3 y 4 de la práctica.

---

##  Paso 2 – EDA simplificado

- Se ha explorado el dataset `attrition_availabledata_07.csv.gz`.
- Se identificaron variables numéricas y categóricas.
- Se detectaron valores nulos y columnas constantes o no informativas (`EmployeeCount`, `Over18`, etc.).
- Se confirmó que el problema es de **clasificación binaria** (`Attrition` = Yes/No).
- El conjunto está **desbalanceado**, con solo un ~16% de la clase "Yes".

---

##  Paso 3 – Evaluación del modelo

- Se dividió el conjunto en **train (2/3)** y **test (1/3)** usando `train_test_split`, con estratificación.
- El conjunto de test se reservará para la evaluación final (outer).
- Se usará `StratifiedKFold` con 5 particiones para validación cruzada (inner).
- Métrica principal: `balanced accuracy`. También se tendrán en cuenta `TPR`, `TNR`, `accuracy` y la matriz de confusión.

---

##  Paso 4 – Modelos básicos: KNN y Árbol

- Se compararon combinaciones de **imputación** (media, mediana) y **escalado** (MinMax, Standard, Robust) usando KNN.
- La mejor combinación fue **media + StandardScaler**.
- Se evaluaron KNN y Árbol con parámetros por defecto, midiendo tiempo y rendimiento.
- Se ajustaron los hiperparámetros más importantes:
  - `k` para KNN → mejor rendimiento con valores bajos (`k = 1 o 2`)
  - `max_depth` para el Árbol → mejora al principio, pero se estabiliza
- Se incluyeron gráficos para visualizar el efecto de los hiperparámetros.
- Ambos modelos mejoran claramente frente a un clasificador trivial.
