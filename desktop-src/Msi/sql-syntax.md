---
description: Las cadenas de consulta SQL para Windows Installer están restringidas a los siguientes formatos.
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: Sintaxis SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1b7d1179a8b6035186a9a5e78f46fdc857ac18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908834"
---
# <a name="sql-syntax"></a>Sintaxis SQL

Las cadenas de consulta SQL para Windows Installer están restringidas a los siguientes formatos.



| Acción                             | Consultar                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Seleccionar un grupo de registros          | Seleccione \[ DISTINCT \] {Column-List} from {table-List} \[ Where {Operation-List} \] \[ order by {Column-List}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| Eliminar registros de una tabla        | ELIMINAR de {Table} \[ donde {Operation-List}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Modificar los registros existentes en una tabla | UPDATE {Table-List} SET {Column} = {Constant} \[ , {Column} = {Constant} \] \[ ,... \] \[ DONDE {Operation-List} \] las consultas Update solo funcionan en columnas de clave no principal.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Agregar registros a una tabla             | Los valores de INSERT INTO {Table} ({Column-List}) ({Constant-List}) los \[ \] datos binarios temporales no se pueden insertar en una tabla directamente mediante las consultas SQL INSERT INTO o Update. Para obtener más información, vea [Agregar datos binarios a una tabla con SQL](adding-binary-data-to-a-table-using-sql.md).<br/>                                                                                                                                                                                                       |
| Agregar una tabla                        | CREATE TABLE {Table} ({Column} {Column type}) \[ \] debe especificar tipos de columna para cada columna al agregar una tabla. Se debe especificar al menos una columna de clave principal para la creación de una nueva tabla. Las posibles sustituciones de {Column type} en las versiones anteriores son: CHAR \[ ({Size}) \] \| character \[ ({Size}) \] \| LONGCHAR \| Short \| int \| Integer \| Long int \| Object \[ not null \] \[ Temporary \] \[ localizable \] \[ , Column... \] \[ ,.. \] . Columna de clave principal \[ , columna \] \[ ,... \] .<br/> |
| Quitar una tabla                     | DROP TABLE {Table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Adición de una columna                       | ALTER TABLE {Table} ADD {Column} {Column type} el tipo de columna debe especificarse al agregar una columna. Las posibles sustituciones de {Column type} en lo anterior son: CHAR \[ ({Size}) \] \| character \[ ({Size}) \] \| LONGCHAR \| Short \| int \| Integer \| Long \| Object \[ not null \] \[ \] \[ \] \[ \] Reverse de forma temporal.<br/>                                                                                                                                                                  |
| Almacenar y liberar tablas temporales     | ALTER TABLE {nombre de tabla} tabla HOLDALTER {nombre de tabla} gratis<br/> El usuario puede usar los comandos HOLD y FREE para controlar el intervalo de vida de una tabla temporal o una columna temporal. El recuento de retención de una tabla se incrementa para cada operación de retención de SQL en esa tabla y se reduce para cada operación de liberación de SQL en la tabla. Cuando se libera el último recuento de retención en una tabla, no se puede tener acceso a todas las columnas temporales. Si todas las columnas son temporales, la tabla deja de estar accesible.<br/>     |



 

Para obtener más información, vea [ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md).

### <a name="sql-grammar"></a>Gramática de SQL

Los parámetros opcionales se muestran entre corchetes \[ \] . Cuando se enumeran varias opciones, los parámetros opcionales se separan mediante una barra vertical.

{Constant} es una cadena o un entero. Una cadena se debe incluir entre comillas simples ' example '. {Constant-List} es una lista delimitada por comas de una o más constantes.

La opción LOCALIZAble establece un atributo de columna que indica que se debe localizar la columna.

Una {Column} es una referencia de columna a un valor de un campo de una tabla.

{Marker} es una referencia de parámetro a un valor proporcionado por un registro enviado con la consulta. Se representa en la instrucción SQL mediante un signo de interrogación?. Para obtener información sobre el uso de parámetros, consulte la función [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) o el método [**Execute**](view-execute.md) .

La sintaxis de Windows Installer SQL no admite el escape de comillas simples (valor ASCII 39) en un literal de cadena. Sin embargo, puede capturar o crear el registro, establecer el campo con la propiedad [**StringData**](record-stringdata.md) o [**IntegerData**](record-integerdata.md) y, a continuación, llamar al método [**Modify**](view-modify.md) . Como alternativa, puede crear un registro y usar los marcadores de parámetros (?) descritos en el método [**Execute**](view-execute.md) . También puede hacerlo mediante las funciones de base de datos [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute), [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)y [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa).

Una cláusula WHERE {Operation-List} es opcional y es una agrupación de operaciones que se va a usar para filtrar la selección. Las operaciones deben ser de los siguientes tipos:

-   {Column} = {columna}
-   {Column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {constante}
-   {Column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {marcador}
-   {Column} es null
-   {Column} no es null

En el caso de los valores de cadena, solo son posibles las operaciones = o <> . Las comparaciones de valores de objeto están limitadas a IS NULL y IS NOT NULL.

Las operaciones individuales se pueden agrupar por operadores AND u OR. La ordenación se puede imponer mediante el uso de paréntesis ().

La cláusula ORDER BY es opcional y produce un retraso inicial durante la ordenación. La ordenación por cadenas agrupará cadenas idénticas, pero no creará alfabéticamente las cadenas.

La cláusula DISTINCt es opcional y no repite registros idénticos en el conjunto de resultados devuelto.

{Table-List} es una lista delimitada por comas de uno o más nombres de tabla denominados {Table} en la combinación.

{Column-List} es una lista delimitada por comas de una o varias columnas de tabla a las que se hace referencia como {Column} seleccionada. Las columnas ambiguas se pueden calificar más como {TableName. Column}. Se puede usar un asterisco como una lista de columnas en una consulta SELECT para representar todas las columnas de las tablas a las que se hace referencia. Al hacer referencia a campos por posición de columna, seleccione las columnas por nombre en lugar de usar el asterisco. No se puede usar un asterisco como una lista de columnas en una consulta INSERT INTO.

Para omitir los nombres de tabla y de columna que entran en conflicto con las palabras clave de SQL, incluya el nombre entre dos marcas de acento grave \` \` (valor ASCII 96). Si un nombre de columna se debe escapar y está calificado como {TableName. Column}, la tabla y la columna se deben escapar individualmente como { \` TableName \` . \` columna \` }. Se recomienda que todos los nombres de tabla y de columna se escapen de este modo para evitar conflictos con palabras reservadas y obtener un rendimiento significativo.

Los nombres de tabla están limitados a 31 caracteres. Para obtener más información, vea [nombres de tabla](table-names.md). Los nombres de tabla y columna distinguen mayúsculas de minúsculas. Las palabras clave de SQL no distinguen mayúsculas de minúsculas.

El número máximo de expresiones en una cláusula WHERE de una consulta SQL está limitado a 32.

Solo se admiten combinaciones internas y se especifican mediante una comparación de columnas de tablas diferentes. No se admiten las combinaciones circulares. Una combinación circular es una consulta SQL que vincula tres o más tablas en un circuito. Por ejemplo, la siguiente es una combinación circular:

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

Las columnas que forman parte de las claves principales de una tabla deben definirse en primer lugar en orden de prioridad, seguidas de cualquier columna de clave no principal. Las columnas persistentes deben definirse antes que las columnas temporales. La secuencia de ordenación de una columna de texto no está definida. sin embargo, los valores de texto idénticos siempre agrupan.

Tenga en cuenta que al agregar o crear una columna, debe especificar el tipo de columna.

Las tablas no pueden contener más de una columna de tipo ' Object '.

El tamaño máximo que se puede especificar explícitamente para una columna de cadena en una consulta SQL es 255. Una columna de cadena de longitud infinita se representa como con el tamaño 0. Para obtener más información, vea [formato de definición de columna](column-definition-format.md).

Para ejecutar cualquier instrucción SQL, se debe crear una vista. Sin embargo, una vista que no crea un conjunto de resultados, como CREATE TABLE o INSERT INTO, no se puede usar con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ni con el método [**Modify**](view-modify.md) para actualizar las tablas a través de la vista.

Tenga en cuenta que no se puede capturar un registro que contenga datos binarios de una base de datos y, a continuación, utilizar ese registro para insertar los datos en una base de datos completamente diferente. Para trasladar datos binarios de una base de datos a otra, debe exportar los datos a un archivo y, a continuación, importarlos en la nueva base de datos a través de una consulta y la función [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) . Esto garantiza que cada base de datos tiene su propia copia de los datos binarios.

 

 




