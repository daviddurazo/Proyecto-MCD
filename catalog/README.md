Como usar datasets.csv

Si encuentras un dataset, recopila la siguiente informacion:

dataset_id
name,
description,
source,
source_url,
access_type,
format,
geographic_level,
start_year,
end_year,
owner,
status : {proposed, approved, rejected} # Se manejaran este tipo de estados para el dataset encontrado
notes

Ejemplo:

INEGI-001
Población por municipio
Población total desagregada por municipio
INEGI
https://...
download
CSV
municipio
2020
2020
NULL
David
proposed
NULL
NULL
Datos del Censo 2020

Una vez tengas esta información recopilada, agrégala al datasets.csv en este formato:

 - dataset_id,name,description,source,source_url,access_type,format,geographic_level,start_year,end_year,owner,status,notes

Una vez tengamos varios datasets encontrados vamos a revisarlos para ver si son útiles, si podemos sacarles informacion relevante y tal,
cambiamos el estado de estos (proposed->approved o proposed->rejected)

Ya con esto empezamos la ingesta, que se vaya llenando la carpeta data/bronze.

Solo los archivos approved se descargan. 

Una vez descargados, calculamos el SHA-256 de cada uno (huella digital, simplemente por auditabilidad e integridad.)
y por ultimo se agrega esta información al ingestions.csv
