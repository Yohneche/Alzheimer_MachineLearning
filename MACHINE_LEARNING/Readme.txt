README.txt
==========

Proyecto: Modelo Predictivo de Alzheimer mediante Machine Learning
Autor: Carlos Yohn Echevarría

------------------------------------------------------------
1. Descripción general
------------------------------------------------------------
Este proyecto desarrolla un modelo predictivo orientado al apoyo al diagnóstico
de la enfermedad de Alzheimer a partir de datos clínicos, cognitivos y funcionales
de pacientes.

El objetivo principal es evaluar la viabilidad de técnicas de Machine Learning
como herramienta de soporte a la toma de decisiones clínicas, mejorando la
detección y clasificación de pacientes según su estado cognitivo.

------------------------------------------------------------
2. Conjunto de datos
------------------------------------------------------------
El conjunto de datos utilizado contiene información clínica de pacientes
clasificados por diagnóstico. Incluye, entre otras, las siguientes variables:

- Puntuaciones cognitivas (MMSE).
- Indicadores de capacidad funcional y autonomía.
- Variables relacionadas con comportamiento y memoria.

El análisis exploratorio mostró diferencias significativas entre los grupos
diagnósticos, destacando la pérdida de autonomía funcional como un indicador clave.

------------------------------------------------------------
3. Análisis exploratorio
------------------------------------------------------------
Durante el análisis exploratorio se estudiaron:

- Distribución de pacientes por diagnóstico, observando un equilibrio razonable
  entre clases.
- Evolución de las variables cognitivas y funcionales, con un descenso progresivo
  del MMSE asociado al avance de la enfermedad.
- Variables de comportamiento y memoria como factores complementarios al diagnóstico.

------------------------------------------------------------
4. Construcción del modelo
------------------------------------------------------------
El proceso de modelado se realizó mediante un pipeline común que incluyó:

- Preprocesado de datos.
- Selección y depuración de variables.
- Entrenamiento y validación de distintos algoritmos de clasificación.

------------------------------------------------------------
5. Depuración de variables
------------------------------------------------------------
Durante el análisis de importancia de variables se detectó un problema de
data leakage: la variable 'ClientID' aparecía con alta importancia predictiva
a pesar de no tener relevancia clínica.

Tras eliminar dicha variable y reconstruir el modelo, se obtuvo una mejora
en la robustez y validez clínica de los resultados.

------------------------------------------------------------
6. Modelos evaluados
------------------------------------------------------------
Se compararon distintos algoritmos de Machine Learning bajo el mismo pipeline:

- Random Forest: accuracy aproximada de 0,92.
- Gradient Boosting: accuracy aproximada de 0,95.
- SVM: accuracy aproximada de 0,83.
- Regresión Logística: accuracy aproximada de 0,83.

El modelo Gradient Boosting fue el que ofreció mejor rendimiento global.

------------------------------------------------------------
7. Evaluación final
------------------------------------------------------------
En la evaluación sobre el conjunto de test, el modelo alcanzó una accuracy
cercana al 95 %, manteniendo un buen equilibrio entre precisión (precision)
y exhaustividad (recall).

------------------------------------------------------------
8. Conclusiones
------------------------------------------------------------
- El modelo permite predecir la enfermedad de Alzheimer con alta fiabilidad.
- Las variables cognitivas y funcionales son determinantes en el diagnóstico.
- La correcta depuración de features es esencial para evitar sesgos.
- El modelo actúa como herramienta de apoyo a la decisión clínica, no como
  sustituto del juicio médico.

------------------------------------------------------------
9. Trabajo futuro
------------------------------------------------------------
Como líneas de trabajo futuro se plantea:

- Ampliar el conjunto de datos con más pacientes.
- Validar el modelo en entornos clínicos reales.
- Incorporar técnicas de interpretabilidad para facilitar su adopción por
  profesionales sanitarios.

------------------------------------------------------------
Fin del documento
------------------------------------------------------------
