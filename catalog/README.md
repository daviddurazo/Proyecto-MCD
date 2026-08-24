# Como usar datasets.csv

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
status : {proposed, approved, rejected}
notes

Se manejaran este tipo de estados para el dataset encontrado

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
