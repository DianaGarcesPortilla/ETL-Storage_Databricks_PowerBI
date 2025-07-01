# ETL-Storage_Databricks_PowerBI

Extracción de datos de ventas trimestrales de ilevo desde Azure Blob Storage, para su transformación en Databricks y conexión con Power BI. 

Se conecta Databricks con la cuenta de almacenamiento de Azure. Se hace uso del almacén de llaves para no publicar claves de acceso en el código.
Una vez leído los datos, el dataframe se escribe en formato Delta Lake y se guarda en el catálogo de Databricks, con el objeto de realizar la corrección del nombre de producto y id de producto en factura específica de la tabla, y llevar el control de versiones o cambios en esta. 

Posteriormente, se enlaza la tabla de Databricks con Power BI desktop mediante dos métodos: ODBC y DirectQuery, para realizar análisis del comportamiento de las ventas.
