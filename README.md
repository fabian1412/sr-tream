# app.py

import streamlit as st
import numpy as np
import matplotlib.pyplot as plt

# Título de la aplicación
st.title("Análisis de Datos Simple")

# Crear un slider
valor = st.slider("Selecciona un valor", 0, 100, 50)

# Mostrar el valor del slider
st.write(f"Valor seleccionado: {valor}")

# Crear algunos datos para graficar
x = np.linspace(0, 10, 100)
y = np.sin(x * (valor / 50))

# Graficar
fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_title("Gráfico Seno")
st.pyplot(fig)
