## Predicción de Emisiones de CO2 en Rwanda

**Integrantes:**

- Laura Cristina Diaz Osorio.
  - C.C: 1018351214
  - Programa de matrícula: Ingeniería Industrial (virtual)

- Juan Felipe Escobar Rendón.
  - C.C:1001416321
  - Programa de matrícula: Ingeniería de Sistemas

Los datos fueron tomados de [Kaggle Competitions]([https://www.kaggle.com/settings/account](https://www.kaggle.com/competitions/playground-series-s3e20/data)):

Para visualizar los archivos, se cargarán los datos desde Kaggle directamente en Google Colab y luego se visualizarán con Pandas.

### Pasos para cargar y visualizar los datos

1. Cargar el archivo JSON de autenticación de Kaggle utilizando Google Colab:
```
from google.colab import files

files.upload()
```
2. Instalar la API de Kaggle:
```
!pip install kaggle
```
3.Mover el archivo JSON de autenticación a la ubicación correcta:
```
!mkdir -p ~/.kaggle
!mv kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
```
4.Descargar los datos de la competición "Playground Series - S3E20" desde Kaggle:
```
!kaggle competitions download -c playground-series-s3e20
```
5.Descomprimir el archivo ZIP descargado:
```
!unzip playground-series-s3e20.zip
```
6.Leer el archivo de entrenamiento en un DataFrame de Pandas:
```
import pandas as pd
df = pd.read_csv('train.csv')
```
7. Visualizar los primeros registros del DataFrame:
```
df.head()
```
