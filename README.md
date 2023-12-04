# PLN_PROYECTO_Axel_Martin_Vega_Espinoza
Proyecto de la unidad 4 para la materia de Ciencia de Datos.     

El siguiente proyecto consiste en emplear el análisis de sentimientos para tratar de predecir las calificaciones de una serie.

El dataset es sobre las calificaciones que recibió la adaptación al "live-action" el anime "OnePiece".

El dataset contiene las reseñas que se recibieron en la plataforma de Netflix, el dataset contiene información como:

<ul>
    <li>Título.</li>
    <li>Reseña.</li>
    <li>Fecha.</li>
    <li>Calificación.</li>
</ul>

__________________________

ETAPA 1: ANÁLISIS EXPLORATORIO DE LOS DATOS.     
Se importan las librerías necesarias, se carga y se muestra información del dataset sobre las calificaciones de la serie “OnePiece”. Se identifican los datos nulos, se muestra la distribución de la columna “Rating” y se determina si alguna columna se puede convertir en categórica.    


ETAPA 2: ANÁLISIS DE SENTIMIENTOS.    
Se hace una función para el pre-procesamiento de los textos, que incluye tokenización, filtrado de palabras de parada y lematización. Se aplica la función a las columnas “Review” y “Title” y se guarda el resultado en nuevas columnas. Se hace otra función para obtener el sentimiento de las palabras usando el SentimentIntensityAnalyzer() y se aplica a las nuevas columnas, guardando el resultado en otras columnas nuevas. Se prepara un dataframe con todas las columnas originales y las creadas previamente.    


ETAPA 3: MACHINE LEARNING.     
Se asignan las variables X e Y con las columnas numéricas y la columna “Rating”, respectivamente, seleccionando solo las filas sin datos nulos. Se divide el dataset en una muestra de entrenamiento y una de prueba, estratificando por la variable objetivo. Se entrenan tres modelos de clasificación: KNN, SVM y RandomForest. Se evalúa el rendimiento de los modelos usando accuracy y RMSE. Se usa el mejor modelo para predecir el “Rating” de las filas con datos nulos y se revisa si son consistentes con las reseñas.