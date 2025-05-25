# Análisis Geográfico y de Costos de Envió - Proyecto

Este repositorio contiene un archivo `.ipynb` que permite analizar datos de ventas y costos de envío de diversas tiendas, utilizando visualizaciones geográficas y estadísticas. El proyecto integra herramientas como Folium para mapas interactivos y matplotlib para visualizaciones adicionales. Este documento explica cómo utilizar el archivo y personalizar el análisis.

---

## **Requisitos Previos**

1. **Lenguaje de Programación:** Python 3.7 o superior.

2. **Bibliotecas Necesarias:** Instalar las siguientes bibliotecas con `pip`:

   ```bash
   pip install pandas folium matplotlib
````

3. **Archivo de Datos:** Asegúrese de tener los datos en formato adecuado (CSV, JSON o integrado en el archivo `.ipynb`) con la siguiente estructura:

   | Producto          | Categoría del Producto | Precio   | Costo de envío | Fecha de Compra | Vendedor        | Lugar de Compra | Calificación | Método de pago     | Cantidad de cuotas | lat     | lon       |
   | ----------------- | ---------------------- | -------- | -------------- | --------------- | --------------- | --------------- | ------------ | ------------------ | ------------------ | ------- | --------- |
   | Asistente virtual | Electrónicos           | 164300.0 | 6900.0         | 16/01/2021      | Pedro Gomez     | Bogotá          | 4            | Tarjeta de crédito | 8                  | 4.60971 | -74.08175 |
   | Mesa de comedor   | Muebles                | 192300.0 | 8400.0         | 18/05/2022      | Beatriz Morales | Medellín        | 1            | Tarjeta de crédito | 4                  | 6.25184 | -75.56359 |

---

## **Pasos para Utilizar el Archivo**

### 1. **Clonar el Repositorio**

Clona este repositorio en tu computadora local:

```bash
git clone https://github.com/usuario/proyecto-analisis-geografico.git
```

### 2. **Abrir el Archivo en Jupyter Notebook**

Accede al directorio clonado y abre el archivo `.ipynb` en Jupyter Notebook o Jupyter Lab:

```bash
cd proyecto-analisis-geografico
jupyter notebook analisis_geografico.ipynb
```

### 3. **Ejecutar el Análisis**

El archivo contiene las siguientes secciones:

#### a. **Carga de Datos**

* Asegúrese de cargar correctamente los datos en un DataFrame utilizando pandas.
* Puede personalizar la ubicación del archivo de datos (si aplica).

#### b. **Mapas Interactivos con Folium**

* Se generan mapas interactivos que muestran los puntos de venta basados en latitud y longitud.
* Incluye un Heatmap que representa la concentración geográfica de las ventas.

#### c. **Análisis de Costos de Envió**

* Gráfico de barras comparativo para analizar los costos promedio de envío entre tiendas.
* Identificación de tendencias y recomendaciones.

### 4. **Visualización de Resultados**

Ejecute cada celda secuencialmente para generar:

* Mapas interactivos que destacan la ubicación geográfica de las ventas.
* Heatmaps para visualizar la concentración de actividades comerciales.
* Gráficos estadísticos sobre el rendimiento de las tiendas y sus costos de envío.

---

## **Personalización del Proyecto**

1. **Agregar Nuevos Datos:** Puede incluir más columnas al DataFrame o datos adicionales para enriquecer el análisis.
2. **Modificar Parámetros:** Personalice el radio del Heatmap o los colores de los marcadores en Folium según las preferencias.
3. **Exportar Resultados:** Genere archivos de salida con los mapas o las visualizaciones gráficas en formato PNG o HTML.

---

## **Ejemplo de Uso**

```python
import folium
from folium.plugins import HeatMap
import pandas as pd

# Cargar datos
datos = {
    'Producto': ['Asistente virtual', 'Mesa de comedor'],
    'lat': [4.60971, 6.25184],
    'lon': [-74.08175, -75.56359]
}
df = pd.DataFrame(datos)

# Crear mapa base
mapa = folium.Map(location=[4.60971, -74.08175], zoom_start=6)

# Agregar marcadores
for _, row in df.iterrows():
    folium.Marker(location=[row['lat'], row['lon']], popup=row['Producto']).add_to(mapa)

# Guardar el mapa como HTML
mapa.save('mapa.html')
```

---

## **Contribuciones**

Se aceptan contribuciones para mejorar el análisis o agregar nuevas funcionalidades. Por favor, realice un fork del repositorio y envíe un pull request con los cambios propuestos.

---

## **Licencia**

Este proyecto está bajo la licencia MIT. Consulte el archivo `LICENSE` para obtener más información.

```
```
