# Sistema de clasificación k-NN y modelado UML  
## Prácticas PRC-6 y PRC-7  

Este proyecto combina los desarrollos realizados en las prácticas PRC-6 y PRC-7, centradas en el diseño, implementación y documentación de un sistema de clasificación basado en el algoritmo k-NN (*k-Nearest Neighbors*), junto con su correspondiente modelado mediante diagramas UML. Todo el código y documentación están integrados en un único repositorio.


## 🧪 PRC-6 – Gestión y ejecución de experimentos

### Objetivo  
Diseñar un sistema capaz de gestionar experimentos reproducibles con un clasificador k-NN sencillo, separando adecuadamente los conjuntos de entrenamiento y prueba, e implementando componentes reutilizables.

### Componentes implementados

- `ExperimentManager`:
  - Divide el conjunto de datos de forma aleatoria pero determinista (usando semillas).
  - Guarda los subconjuntos generados en archivos CSV.
  - Ejecuta experimentos usando el clasificador k-NN.
  - Muestra por consola:
    - Predicciones
    - Matriz de confusión
    - Precisión predictiva
  - Genera informes en archivos `.txt`.

- `DataSet`:
  - Clase que encapsula la carga, almacenamiento y manipulación de datos.
  - Soporta CSV y estructuras internas para atributos y clases.

### Diagramas UML asociados

📂 `/docs/diagrams/deActividad`:  
- División aleatoria de datos  
- Ejecución del experimento  
- Generación de informe  

📂 `/docs/diagrams/deEstado`:  
- Estados del gestor de experimentos  
- Flujo de transición entre carga, ejecución y análisis  

---

## 🧠 PRC-7 – Clasificador k-NN y modelado detallado

### Objetivo  
Ampliar el sistema con la implementación de un clasificador k-NN configurable y modelar su comportamiento mediante diagramas de interacción.

### Componentes nuevos

- `KNNClassifier`:
  - Permite configurar el valor de *k* y la métrica de distancia (Euclidiana, Manhattan, etc.).
  - Clasifica nuevas instancias mediante votación de los *k* vecinos más cercanos.
  - Se integra con `ExperimentManager`.

- Ampliación de `ExperimentManager`:
  - Llama al clasificador para cada instancia del conjunto de prueba.
  - Calcula la matriz de confusión y precisión global.

### Diagramas UML asociados

📁 `/docs/`:

📌 `sequence_classification_instance.svg`:  
➡️ Describe el proceso paso a paso desde que una instancia es enviada al clasificador hasta que se obtiene la predicción.

📌 `sequence_dataset_split.svg`:  
➡️ Muestra cómo se divide el dataset original en entrenamiento y prueba mediante una semilla.

📌 `communication_confusion_matrix.svg`:  
➡️ Describe cómo se calculan y representan los resultados tras ejecutar el experimento completo.

---



## 📜 Licencia

Este proyecto está licenciado bajo MIT License.  
Consulta el archivo `LICENSE` para más información.

---## 🧪 PRC-6 – Gestión y ejecución de experimentos

### Objetivo  
Diseñar un sistema capaz de gestionar experimentos reproducibles con un clasificador k-NN sencillo, separando adecuadamente los conjuntos de entrenamiento y prueba, e implementando componentes reutilizables.

### Componentes implementados

- `ExperimentManager`:
  - Divide el conjunto de datos de forma aleatoria pero determinista (usando semillas).
  - Guarda los subconjuntos generados en archivos CSV.
  - Ejecuta experimentos usando el clasificador k-NN.
  - Muestra por consola:
    - Predicciones
    - Matriz de confusión
    - Precisión predictiva
  - Genera informes en archivos `.txt`.

- `DataSet`:
  - Clase que encapsula la carga, almacenamiento y manipulación de datos.
  - Soporta CSV y estructuras internas para atributos y clases.


## 🧠 PRC-7 – Clasificador k-NN y modelado detallado

### Objetivo  
Ampliar el sistema con la implementación de un clasificador k-NN configurable y modelar su comportamiento mediante diagramas de interacción.

### Componentes nuevos

- `KNNClassifier`:
  - Permite configurar el valor de *k* y la métrica de distancia (Euclidiana, Manhattan, etc.).
  - Clasifica nuevas instancias mediante votación de los *k* vecinos más cercanos.
  - Se integra con `ExperimentManager`.

- Ampliación de `ExperimentManager`:
  - Llama al clasificador para cada instancia del conjunto de prueba.
  - Calcula la matriz de confusión y precisión global.

### Diagramas UML asociados

📁 `/docs/`: Contiene los 2 informes de las practicas 6 y 7 asi como los diagramas

---
