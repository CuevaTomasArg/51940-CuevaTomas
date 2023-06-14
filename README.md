# 51940-CuevaTomas
---
Dentro de este repositorio se encuentra el proceso del proyecto final del curso "Data Engineering flex" de Coderhouse.

## Contenido
---
Dentro del repositorio encontraremos los siguiente archivos y carpetas relevantes:
* DB/ : Dentro se encontraran los datos extraidos de la API de CoinGecko

* Dockerfile: Este Dockerfile construirá una imagen Docker basada en Jupyter Notebook que incluirá las librerías Pandas y Requests instaladas, copiará todos los archivos .ipynb desde el contexto de construcción al directorio de trabajo dentro de la imagen y establecerá ese directorio como el directorio de trabajo predeterminado. Esto proporciona un entorno listo para ejecutar y trabajar con archivos Jupyter Notebook que utilizan las librerías mencionadas.

* entrega1/ : En esta carpeta se encuentran los archivos correspondientes a la entrega 1, creacion de tabla en redshift y lectura de JSON extraido de una API con sus trasformaciones de datos correspondientes con el uso de Pandas.

## Configuracion del entorno

1. construir la imagen
```bash
docker build -t jupyter-env .
```
2. Ejecutar el contenedor
```bash
docker run -p 8888:8888 -v <ruta_absoluta_al_directorio_local>:/home/jovyan/work jupyter-env
```

```bash
#en mi caso 
docker run -p 8888:8888 -v "C:\\Users\tomas\OneDrive\Escritorio\DataEngineer\ProyectoFinalCoderhouse:/home/jovyan/work" jupyter-env
```

Con esto ya podras ejecutar los bloques de codigo de los notebooks de este repositorio 