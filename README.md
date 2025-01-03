## Jupyter Notebook en Visual Studio Code
Introducción a GeoPandas usando Jupyter Notebook en Visual Studio Code pero usando el kernel del entorno GIS de Anaconda.

### Documentación

Verificar el repositorio remoto
```ruby
git remote show origin
git remote -v
```

Cambiar de repositorio
```ruby
git remote remove origin
git remote add origin /url/
```

En caso de que rechace el push
```ruby
git fetch origin
git reset --hard origin/main
git push -f origin main
```

Agregar commits a GitHub
```ruby
git status
git add .
git commit -m "acción" # "n" files changed"
git push
```

## R-tree Spatial Indexing with Python (S2)

Practicar la indexación espacial que explica [Geoff Boeing](https://geoffboeing.com/2016/10/r-tree-spatial-index-python/) usando GeoPandas. En este caso usar los geodataframes usados anteriormente en este archivo.

## Hierarchical Hexagonal Geospatial Indexing System (H3)

Instalar la librería de [H3](https://h3geo.org/) en Anaconda Powershell Prompt dentro del environment GIS mediante ```conda config --add channels conda-forge```, ```conda install h3``` y ```conda install h3-py``` ya que está en uso el kernel de Anaconda, que es donde están las librerías instaladas.

Esta librería contiene funciones para convertir latitudes y longitudes en strings que representan los centroides de las celdas hexagonales. Los hexágonos tienen ventajas claras sobre las celdas de cuadrados, ya que ofrecen tamaños de celdas más uniformes y menos efectos de bordes, lo que los hace perfectos para los análisis geoespaciales. H3 tiene una resolución jerárquica y posee 16 niveles de resolución, desde una celda muy grande hasta celdas extremadamente pequeñas. Es muy eficiente para realizar operaciones geoespaciales como cálculos de distancia, contención, agregación de datos, etc. Algunos datos importantes en la [documentación](https://h3geo.org/docs/) del sistema.

```ruby
la función h3.geo_to_h3 se suplantó en la nueva versión por h3.latlng_to_cell
```
Los desarrolladores dicen que la última versión es la v4. Puedo ver [este repositorio](https://uber.github.io/h3-py/polygon_tutorial.html) para las operaciones con polígonos y también existe uno para la [versión 4 completa](https://uber.github.io/h3-py/api_quick.html).

## Conocimiento importante para seguir avanzando
### Anaconda > Environments > Kernel con librerías cargadas en Anaconda PowerShell Prompt
Librerías: pandas, geopandas, matplotlib, folium, H3

### PostgreSQL > PostGIS (QGIS)
Existen ejemplos de trabajos realizados con H3 dentro de PostGIS

### Visual Studio Code > Jupyter Notebook > Python
Librerías: pandas, geopandas, matplotlib, folium, h3

### ETL Software (Extract, Transform and Load) > FME Desktop
Visualizador SIG de escritorio. Input, gestión, transformación y output de datos geoespaciales. Se puede trabajar con extensiones y librerías