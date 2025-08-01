Este conjunto de datos proporciona datos sintéticos pero realistas para analizar y pronosticar la demanda de inventario en tiendas minoristas. Contiene más de 73 000 filas de datos diarios de múltiples tiendas y productos, incluyendo atributos como ventas, niveles de inventario, precios, clima, promociones y días festivos.

El conjunto de datos es ideal para practicar tareas de aprendizaje automático como la previsión de la demanda, la fijación dinámica de precios y la optimización del inventario. Permite a los científicos de datos explorar técnicas de previsión de series temporales, estudiar el impacto de factores externos como el clima y los días festivos en las ventas y crear modelos avanzados para optimizar el rendimiento de la cadena de suministro.


Sistema de Previsión de Demanda para Retail
1. 🎯 Propuesta de Valor / Objetivo del Proyecto
Desarrollar un modelo de Machine Learning para predecir con precisión la demanda diaria de productos en cada tienda.

Impacto Principal:

Optimizar el inventario: Reducir costos por exceso de stock.

Maximizar las ventas: Evitar pérdidas por falta de producto (roturas de stock).

Automatizar decisiones: Pasar de una gestión de inventario reactiva a una proactiva y basada en datos.

2. 🗂️ Recursos Clave
Dataset: retail_store_inventory.csv, conteniendo datos históricos de ventas, inventario, precios, promociones y factores externos desde 2022 hasta 2024.

Stack Tecnológico:

Lenguaje: Python

Librerías Principales: Pandas (Manipulación), Scikit-learn (Preprocessing), XGBoost (Modelado), Matplotlib/Seaborn (Visualización).

3. ⚙️ Actividades Clave / Metodología
El proceso se estructuró como un problema de previsión de series temporales:

Limpieza de Datos: Identificación y manejo de valores ausentes para asegurar la calidad del dataset.

Ingeniería de Características (Feature Engineering):

Extracción de Atributos de Fecha: Se descompuso la columna Date en mes, día_de_la_semana, semana_del_año para capturar estacionalidades.

Creación de Lags y Medias Móviles: Se generaron características basadas en ventas pasadas (ej: ventas del día anterior, media de la última semana) para capturar tendencias y la dinámica temporal.

Modelado y Entrenamiento:

Modelo Utilizado: XGBoost, un algoritmo de Gradient Boosting potente y eficaz para datos tabulares.

Validación Temporal: Se dividieron los datos de forma cronológica (entrenamiento con datos antiguos, prueba con los más recientes) para simular un escenario real de pronóstico.

Evaluación del Modelo: Se midió el rendimiento utilizando métricas de regresión clave para cuantificar la precisión del pronóstico.

¡Excelentes resultados! Un R² de 0.9935 es un número excepcionalmente bueno y demuestra que el modelo es muy preciso.

Aquí tienes el Canvas de Proyecto actualizado con tus métricas. Está listo para que lo incluyas en tu portafolio.

Project Canvas: Sistema de Previsión de Demanda para Retail
1. 🎯 Propuesta de Valor / Objetivo del Proyecto
Desarrollar un modelo de Machine Learning para predecir con precisión la demanda diaria de productos en cada tienda.

Impacto Principal:

Optimizar el inventario: Reducir costos por exceso de stock.

Maximizar las ventas: Evitar pérdidas por falta de producto (roturas de stock).

Automatizar decisiones: Pasar de una gestión de inventario reactiva a una proactiva y basada en datos.

2. 🗂️ Recursos Clave
Dataset: retail_store_inventory.csv, conteniendo datos históricos de ventas, inventario, precios, promociones y factores externos desde 2022 hasta 2024.

Stack Tecnológico:

Lenguaje: Python

Librerías Principales: Pandas (Manipulación), Scikit-learn (Preprocessing), XGBoost (Modelado), Matplotlib/Seaborn (Visualización).

3. ⚙️ Actividades Clave / Metodología
El proceso se estructuró como un problema de previsión de series temporales:

Limpieza de Datos: Identificación y manejo de valores ausentes para asegurar la calidad del dataset.

Ingeniería de Características (Feature Engineering):

Extracción de Atributos de Fecha: Se descompuso la columna Date en mes, día_de_la_semana y semana_del_año para capturar estacionalidades.

Creación de Lags y Medias Móviles: Se generaron características basadas en ventas pasadas (ej: ventas del día anterior, media de la última semana) para capturar tendencias.

Modelado y Entrenamiento:

Modelo Utilizado: XGBoost, un algoritmo de Gradient Boosting potente y eficaz para datos tabulares.

Validación Temporal: Se dividieron los datos de forma cronológica (entrenamiento con datos antiguos, prueba con los más recientes) para simular un escenario real de pronóstico.

Evaluación del Modelo: Se midió el rendimiento utilizando métricas de regresión clave para cuantificar la precisión del pronóstico.

4. 📈 Resultados y Métricas de Éxito
Métricas del Modelo:

R² (Coeficiente de Determinación): 0.9935 — El modelo es capaz de explicar el 99.35% de la variabilidad en las ventas, lo que indica un ajuste casi perfecto a los datos.

MAE (Error Absoluto Medio): 7.54 — En promedio, el pronóstico del modelo se desvía en aproximadamente 8 unidades del número real de ventas diarias. Un error muy bajo que demuestra su alta precisión.

KPIs de Negocio (Impacto Potencial):

Alta Fiabilidad del Pronóstico: Permite tomar decisiones de inventario con un alto grado de confianza.

Reducción de Roturas de Stock: Potencial para reducir significativamente la falta de productos y maximizar los ingresos.

Optimización de Costos de Inventario: Reducción de los costos asociados a mantener productos que no se venden.

5. 👥 Usuarios Finales / Stakeholders
Gerentes de Tienda: Para planificar el stock diario y la disposición del personal.

Analistas de Inventario: Para automatizar las órdenes de compra y gestionar los niveles de stock a nivel central.

Equipo de Marketing: Para medir el impacto de promociones y planificar campañas futuras.

6. 🚀 Próximos Pasos y Mejoras Futuras
Experimentar con otros modelos: Probar modelos específicos para series temporales como SARIMA o Prophet para comparar rendimientos.

Hyperparameter Tuning: Optimizar los hiperparámetros de XGBoost (usando GridSearchCV o RandomizedSearchCV) para exprimir al máximo el rendimiento del modelo.

Análisis de Factores Externos: Cuantificar el impacto real de variables como Weather Condition o Holiday/Promotion en las ventas.

Despliegue (Deployment): Empaquetar el modelo en una API (con FastAPI/Flask) o crear un dashboard interactivo (con Streamlit/Dash) para que los usuarios finales puedan consumir los pronósticos fácilmente.
