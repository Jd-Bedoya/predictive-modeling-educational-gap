README

## Acceso a tecnología y puntaje en Saber 11: un modelo de regresión (ODS 4)

###  Descripción del Proyecto
Este proyecto de ciencia de datos analiza la relación entre el **acceso a tecnología en el hogar** (computador e internet) y el **puntaje global en las pruebas Saber 11** en Colombia, controlando por variables socioeconómicas clave como el estrato de la vivienda y el nivel educativo de los padres. El trabajo se enmarca dentro del **Objetivo de Desarrollo Sostenible 4 (ODS 4): Educación de Calidad**, buscando aportar evidencia cuantitativa para la toma de decisiones en políticas públicas de conectividad e infraestructura tecnológica educativa.

---

###  Pregunta de Negocio
* **Pregunta:** ¿Cuál es el puntaje global esperado de un estudiante en Saber 11 según su acceso a internet y computador en el hogar, a igualdad de nivel socioeconómico?
* **Audiencia / Quién lo usaría:** Secretarías de Educación, Ministerio de Educación y programas de conectividad (como MinTIC).
* **Decisión que apoya:** Priorizar la asignación de subsidios de conectividad y equipos tecnológicos en los perfiles de estudiantes con menor puntaje esperado y en las instituciones educativas donde más se concentran.
* **Tipo de problema:** Regresión (predicción de una variable continua).
* **Variable objetivo:** `punt_global` (Puntaje total en la prueba Saber 11, en escala de 0 a 500).
* **Fuente de datos:** API oficial de [Resultados únicos Saber 11 (ICFES) en datos.gov.co](https://www.datos.gov.co/Educaci-n/Vista-Resultados-nicos-Saber-11/d5t8-3yqf).

---

###  Tecnologías y Librerías Utilizadas
El análisis y modelado se realizaron utilizando Python a través de las siguientes librerías de open-source:
* **Manipulación y análisis de datos:** `pandas`, `numpy`
* **Visualización de datos:** `matplotlib`, `seaborn`
* **Modelado de Machine Learning:** `scikit-learn` (`LinearRegression`, `RandomForestRegressor`, métricas de evaluación).

---

###  Estructura del Cuaderno
El cuaderno de trabajo (`.ipynb`) está estructurado bajo una metodología analítica rigurosa:
1. **Pregunta de negocio:** Definición del problema, alcance y utilidad práctica.
2. **Carga y descripción de los datos:** Extracción de una muestra de 50,000 registros desde la API y revisión estructural.
3. **Análisis Exploratorio de Datos (EDA):** Verificación de nulos, atípicos (métrico IQR) y gráficos de distribución y brechas por estrato y educación parental.
4. **Preparación de datos:** Limpieza, codificación de variables categóricas mediante `get_dummies` y partición de datos (80% entrenamiento / 20% prueba).
5. **Modelado:** Entrenamiento y comparación de un modelo de Regresión Lineal (con tecnología), un modelo de Random Forest y un modelo base de control (sin variables tecnológicas).
6. **Evaluación:** Comparación de métricas de desempeño ($MAE$, $RMSE$ y $R^2$), análisis de coeficientes e identificación de perfiles de menor puntaje esperado.
7. **Conclusiones y limitaciones:** Hallazgos principales, recomendaciones de acción concreta y discusión crítica sobre causalidad y sesgos de los datos.

---

###  Cómo ejecutar el proyecto
1. Clona este repositorio o descarga el archivo del cuaderno Jupyter (`.ipynb`).
2. Asegúrate de tener instalado Python 3 junto con las librerías requeridas (`pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`).
3. Abre el cuaderno en Jupyter Notebook, JupyterLab o Google Colab y ejecuta las celdas secuencialmente. El conjunto de datos se descarga directamente en línea mediante la API pública de datos.gov.co. No omitas nada
