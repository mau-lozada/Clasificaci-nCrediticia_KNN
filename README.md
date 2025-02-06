# ClasificacionCrediticia_KNN
# 📊 Clasificación de Morosidad Crediticia con KNN 🏦

Este proyecto utiliza el algoritmo **K-Nearest Neighbors (KNN)** para predecir si un cliente pagará su crédito (**Clase 1**) o será moroso (**Clase 0**) en función de su edad y monto de crédito otorgado.

## 📂 **Estructura del Proyecto**

## 📄 **Dataset**
- **Registros:** 200 clientes
- **Variables:**
  - `edad` 📅: Edad del cliente.
  - `credito` 💰: Monto del crédito otorgado.
  - `cumplio` ✅❌: **(1) Pagó | (0) No pagó**.

### 🔍 **Insights Clave**
- **Edad promedio:** 37 años (Rango: 18 - 57 años).
- **Monto de crédito promedio:** $289,946 (Rango: $100K - $596K).
- **Distribución de pagos:**
  - **83.5%** de los clientes **pagaron** su crédito.
  - **16.5%** de los clientes fueron **morosos**.
- **Observación:** ⚠ Hay un **desequilibrio de clases**, lo que afecta el rendimiento del modelo.

## 🎨 **Visualización de Datos**
📌 **Distribución de clientes según edad y monto de crédito:**

![image](https://github.com/user-attachments/assets/d11917b8-aa68-4959-a5e8-b4df13878389)


🔹 **Clase 1 (Pagó):** ⭐ Azul  
🔹 **Clase 0 (Moroso):** ❌ Rojo  
🔹 **Tendencia:** No hay una correlación clara entre la edad y el pago, pero los morosos parecen estar en montos más altos.

---

## 🔧 **Preprocesamiento y Validación**
✔ **Escalado de variables** con **MinMaxScaler** (valores entre 0 y 1).  
✔ **Validación cruzada (K-Fold Estratificado, K=5)** para evitar overfitting.  
✔ **Matriz de confusión** para evaluar errores en la predicción.  

### 📊 **Resultados del Modelo KNN**
- **Precisión Promedio:** ✅ **85.00%** (±5.50%)
- **Clase 1 (Pagó):** **Recall = 98%**
- **Clase 0 (Moroso):** **Recall = 55% (riesgo alto de falsos negativos)**

---

## 🔮 **Predicción de Nuevo Cliente**
Ejemplo: **Cliente con 35 años y un crédito de $350,000**  

📊 **Resultados**  
| Característica | Valor |
|--------------|------|
| **Edad** | 35 años |
| **Monto de Crédito** | $350,000 |
| **Predicción** | 🟢 **Pagará (Clase 1)** |
| **Probabilidad de No Pago** | 22% |
| **Probabilidad de Pago** | 78% |

📝 **Interpretación**: El cliente se encuentra en una zona donde la mayoría de los clientes pagaron, por lo que el modelo predice que **pagará** con un 78% de probabilidad.

---

## 🚀 **Cómo Usar el Proyecto**
1️⃣ **Clona el repositorio**
```bash
git clone https://github.com/tuusuario/knn-morosidad.git
cd knn-morosidad


