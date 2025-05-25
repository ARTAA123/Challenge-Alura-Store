# Análisis Geográfico y de Costos de Envió - Proyecto

Este repositorio contiene un archivo `.ipynb` que permite analizar datos de ventas y costos de envío de diversas tiendas, utilizando visualizaciones geográficas y estadísticas. El proyecto integra herramientas como Folium para mapas interactivos y matplotlib para visualizaciones adicionales. Este documento explica cómo utilizar el archivo y personalizar el análisis.

---

## **Estructura del Proyecto**

El repositorio contiene los siguientes archivos:

- `analisis_geografico.ipynb`: Notebook principal con el análisis de datos y visualizaciones.
- `LICENSE`: Detalles de la licencia del proyecto.

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

## **Ejemplos de Visualizaciones e Insights**

1. **Mapa Interactivo:**

   * Muestra los puntos de venta geolocalizados por latitud y longitud.
   * Los marcadores permiten explorar información detallada de cada producto.

   ![Ejemplo Mapa](assets/mapa_ejemplo.png)

2. **Heatmap de Ventas:**

   * Destaca la concentración geográfica de ventas.
   * Insight: Las áreas urbanas tienen una mayor densidad de ventas.

   ![Heatmap](assets/heatmap_ejemplo.png)

3. **Gráfico Comparativo de Costos de Envío:**

   * Muestra las diferencias en los costos promedio de envío entre tiendas.
   * Insight: La tienda 4 tiene el costo de envío más eficiente, mientras que la tienda 1 requiere ajustes.

   ![Gráfico de Barras](assets/costos_envio.png)

---

## **Pasos para Utilizar el Archivo**

### 1. **Clonar el Repositorio**

```bash
git clone https://github.com/usuario/proyecto-analisis-geografico.git
```

### 2. **Abrir el Archivo en Jupyter Notebook**

```bash
cd proyecto-analisis-geografico
jupyter notebook analisis_geografico.ipynb
```
### En Google Colaboratory descarga el archivo y cargalo en Colaboratory.

### 3. **Ejecutar el Análisis**

Ejecute cada celda secuencialmente para generar:

* Mapas interactivos que destacan la ubicación geográfica de las ventas.
* Heatmaps para visualizar la concentración de actividades comerciales.
* Gráficos estadísticos sobre el rendimiento de las tiendas y sus costos de envío.

---

## **Contribuciones**

Se aceptan contribuciones para mejorar el análisis o agregar nuevas funcionalidades. Por favor, realice un fork del repositorio y envíe un pull request con los cambios propuestos.

---

## **Licencia**

Este proyecto está bajo la licencia MIT. Consulte el archivo `LICENSE` para obtener más información.
