# Clasificación de Opiniones con Regresión Logística

Este colab tiene como objetivo **clasificar declaraciones** utilizando **Regresión Logística**. 

---

## Dataset utilizado

Se trabajó con el archivo `dataset_train_95.csv`, que contiene las siguientes columnas:

- `id`  
- `autor`  
- `declaracion`  
- `etiqueta`  
- `palabras_clave`  
- `tweet`  
- `respuesta_mayoria_5_etiquetas`  
- `respuesta_mayoria_3_etiquetas`

Durante la verificación inicial se comprobó que **no existían valores nulos** en ninguna columna.

---

## División de datos

Se combinaron las columnas: `autor`, `declaracion`, `palabras_clave`, `tweet`, `respuesta_mayoria_5_etiquetas`, `respuesta_mayoria_3_etiquetas`.  
Posteriormente, los datos se dividieron en:

- **Entrenamiento:** 90%  
- **Prueba:** 10%

Utilizando la función `train_test_split` de `scikit-learn`.

---

## Transformación del texto

Para que el modelo pueda interpretar los textos, se utilizó **CountVectorizer**, que transforma las palabras en vectores numéricos según su frecuencia.  
De esta forma, el modelo puede aprender patrones de palabras asociados a las etiquetas de clasificación.

---

## Entrenamiento del modelo

Se empleó **Regresión Logística** con la librería `scikit-learn`. 

---

## Predicción 

Para generar predicciones se utilizó el archivo `dataset_test_5_sin_etiqueta.csv`.
Este conjunto de datos también carecía de valores nulos, por lo que se aplicó el mismo proceso antes de realizar la predicción.
Y para finalizar se generó el archivo `submission22.csv` que posterior mente fue publicado en la página `https://guilleu.github.io/` para rankear el modelo.
