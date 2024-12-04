# Notebook_4-AzureSQL

Se va hacer una conexion de Azure postgreSQL servidor flexible con Azure databricks y luego poder hacer consultas en python y/o scala.

En esta parte se va hacer las cosas de una forma distinta como en psotgreSQL no hay datos por defecto.

1. En Azure crearmos una area de trabajo en Azure Databricks.
```
import requests # Obtener la IP pública del nodo
public_ip = requests.get('https://api.ipify.org').text
print(f"La IP pública del nodo es: {public_ip}")
```

2. Crear Azure Database for PostgreSQL servidor flexible.
* En redes debemos poder la IP de Azure Databricks. que obtenemos al ejecutar el codigo que se muestra en el punto 1.
  
En la caperta Notebook 4 esta los notebook que se hizo en Azure Databricks
* PostgreSQL Pyspark
* PostgreSQL Scala
  en estos dos cuadernos esta la conexion de Azure postgresql con Azure Databricks usando pyspark y scala.
  Como no habia una base de datos, para tener datos y poder hacer consultas se hizo lo siguiente
  se subio los archivos .sql al dbfs y luego se lee el archivo, se crea una tabla y luego se guardar en     
   postgresql
* Consultas SQL - Pyspark
* Consulta SQL - Scala
  estos cuardenos se vuelve hacer la conexion con postsql y hacemos consultas ya obteniendo los datos de   
  postgre que se ha han guardado antes.

luego se ha ce una conexion con PowerBI accediendo con el user y password que se uso al crear Azure PosgreSQL
