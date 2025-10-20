# 🧮 Calculadora de Respuesta Tumoral

**Descripción:**  
Calculadora para obtener los **rangos orientativos de respuesta tumoral** en enfermedades como **mieloma**, **linfoma** y **otras**.  
Permite estimar el porcentaje de disminución entre el valor basal (diagnóstico) y el valor post-tratamiento según la fórmula:

\[
\text{Respuesta} = \bigl[((a/b) \times 100) - 100 \bigr] \times (-1)
\]

---

## ⚙️ Funcionamiento

El programa en Python calcula la disminución porcentual y clasifica la respuesta en una de las siguientes categorías:

| Clasificación | Criterio |
|----------------|-----------|
| **Completa** | Desaparición total del componente (b = 0) |
| **Muy buena respuesta parcial** | Disminución > 90 % |
| **Respuesta parcial** | Disminución entre 50 % y 90 % |
| **Sin respuesta** | Disminución < 50 % |
| **Progresión** | Aumento del valor post-tratamiento |

---

## 💻 Archivos incluidos

- **`index.html`** → Página descriptiva con notas explicativas y el código en Python.  
- **`respuesta_tumoral.py`** → Script Python para ejecución local o en Google Colab.

---

## 🧪 Ejemplo de uso en Python

```python
# Ejecutar en Google Colab o terminal
from respuesta_tumoral import evaluar_respuesta
resultado = evaluar_respuesta("mieloma", a=3.5, b=0.2)
print(resultado)
