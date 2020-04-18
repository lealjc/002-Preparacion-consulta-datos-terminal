# 002-Preparacion-consulta-datos-terminal
Básico / Introducción a Base de Datos / Preparación y consulta de datos desde la terminal / Postwork


<hr>
<b>Estos son las instrucciones que utilice para el Postwork de la sesión 2.</b>

<hr>

- Analizando el contenido de un archivo:

head cat_ur.dat

head estadis.dat
<br>
<br>

- Reemplazando secciones de un archivo:

sed "s/DELEGACION/DEL./g" cat_ur.dat | head

sed "s/DELEGACION/DEL./g" cat_ur.dat > resultados.csv

head resultados.csv
<br>
<br>

- Ya que los archivos están en formato CSV, entonces se puede iniciar a realizar consultas usando los comandos grep y wc

grep -a CH resultados.csv | head

grep -a CH resultados.csv | wc

grep -a DF resultados.csv | head

grep -a DF resultados.csv | wc
<br>
<br>

- Se cuenta en número de líneas o registros

grep -a DF resultados.csv > resultados-DF.csv

sed "s/, 12,/, DIC,/g" estadis.dat > estadis.csv
<br>
<br>

- ...si quieres encontrar todos los registros que inicien con cierta palabra puedes usar:

grep -aE ^2019 estadis.csv | head
