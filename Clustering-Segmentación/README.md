# 📨 Clustering MVP - Segmentación de Clientes para Marketing

Este proyecto es una práctica de segmentación de usuarios basada en interacciones por correo electrónico. Se utiliza K-Means para construir un **MVP (Producto Mínimo Viable)** que permita agrupar clientes según su comportamiento, con potencial aplicación en campañas de marketing personalizadas.

---

## 📊 Dataset

El dataset contiene información de campañas de email marketing por usuario o interacción, incluyendo variables relacionadas a entregabilidad, comportamiento y respuesta a correos.

### Variables disponibles:

| Variable      | Descripción                                                                  |
| ------------- | ---------------------------------------------------------------------------- |
| `Id`          | Identificador único de campaña, usuario o interacción                        |
| `send`        | Número de correos enviados                                                   |
| `bounce`      | Correos que rebotaron (no llegaron al destinatario)                          |
| `open`        | Cantidad de aperturas del correo                                             |
| `click`       | Cantidad de clics en enlaces dentro del correo                               |
| `Total`       | Suma total de interacciones registradas (envíos, aperturas, clics, etc.)     |
| `Comprador`   | Variable binaria: 1 si realizó una compra, 0 si no                           |
| `hour`        | Hora promedio de interacción (puede ser decimal, por ejemplo, 19.75 = 19:45) |
| `day_of_week` | Día promedio de interacción (por ejemplo, 3.5 = entre miércoles y jueves)    |

📌 *Nota: La variable `Comprador` no especifica si representa comportamiento histórico completo o solo del último año.*

---

## 🚀 Objetivo del proyecto

Construir un modelo de segmentación de clientes mediante K-Means, que permita:

* Agrupar usuarios según patrones de interacción.
* Analizar el comportamiento de cada grupo.
* Sentar las bases para futuras estrategias de marketing personalizadas.

---

## 🧠 Flujo del proyecto (`clustering_mvp_kmeans.ipynb`)

1. **Carga de datos y exploración inicial**
2. **Selección de variables relevantes para segmentar**
3. **Normalización de variables con `StandardScaler`**
4. **Determinación del número óptimo de clusters** con método silhouette
5. **Entrenamiento de K-Means**
6. **Asignación de etiquetas y análisis de perfiles de clusters**
7. **Comparación con variable `Comprador`**

---

## 📌 Cómo usar este proyecto

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/GabiMiranda05/Practice-Data-Science.git
   cd Practice-Data-Science/Clustering-Segmentación
   ```

2. Ejecutar el notebook `clustering_mvp_kmeans.ipynb` con Jupyter o Google Colab.

3. Analizar los segmentos generados y sus características.

---

## 🔍 Resultados esperados

* Segmentos diferenciables por nivel de interacción (alta vs. baja), rebote, horario de conexión, etc.
* Identificación de perfiles que podrían ser priorizados en campañas de remarketing.
* Cruce preliminar con variable `Comprador` para evaluar relación entre clusters y conversión.

---

## ✏️ Próximos pasos sugeridos

* Validar clusters con datos nuevos o posteriores.
* Enriquecer el modelo con variables temporales o de engagement histórico.
* Usar el MVP como base para un dashboard interactivo o motor de recomendación de campañas.
