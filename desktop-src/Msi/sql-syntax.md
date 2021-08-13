---
description: Las SQL de consulta para Windows Installer están restringidas a los siguientes formatos.
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: Sintaxis SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6512f52ae687ee3f95a00f104c7cdfa251c878b649809faeb86c73bdcf82bf84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624679"
---
# <a name="sql-syntax"></a>Sintaxis SQL

Las SQL de consulta para Windows Installer están restringidas a los siguientes formatos.



| Acción                             | Consultar                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selección de un grupo de registros          | SELECT \[ DISTINCT \] {column-list} FROM {table-list} \[ WHERE {operation-list} \] \[ ORDER BY {column-list}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| Eliminación de registros de una tabla        | DELETE FROM {table} \[ WHERE {operation-list}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Modificación de los registros existentes en una tabla | UPDATE {table-list} SET {column}= {constant} \[ , {column}= {constant} \] \[ , ... \] \[ Las consultas WHERE {operation-list} \] UPDATE solo funcionan en columnas de clave no principales.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Agregar registros a una tabla             | INSERT INTO {table} ({column-list}) VALUES ({constant-list}) TEMPORARY Binary data cannot be inserted into a table directly using the INSERT INTO or \[ UPDATE SQL \] queries. Para obtener más información, vea [Agregar datos binarios a una](adding-binary-data-to-a-table-using-sql.md)tabla mediante SQL .<br/>                                                                                                                                                                                                       |
| Agregar una tabla                        | CREATE TABLE {table} ( {column} {column type}) Se deben especificar tipos de columna HOLD para cada columna al \[ \] agregar una tabla. Se debe especificar al menos una columna de clave principal para la creación de una nueva tabla. Las posibles sustituciones para {tipo de columna} en el anterior son: CHAR \[ ( {size} ) \] \| CHARACTER ( \[ {size} ) \] \| LONGCHAR \| SHORT INT INTEGER LONG OBJECT NOT NULL \| TEMPORARY \| \| \| \[ \] \[ \] \[ LOCALIZABLE \] \[ , column... \] \[ , ... \] Columna PRIMARY KEY \[ , columna , ... \] \[ \] .<br/> |
| Quitar una tabla                     | DROP TABLE {table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Adición de una columna                       | ALTER TABLE {table} ADD {column} {column type}El tipo de columna debe especificarse al agregar una columna. Las posibles sustituciones para {tipo de columna} en el anterior son: CHAR \[ ( {size} ) \] \| CHARACTER ( \[ {size} ) \] \| LONGCHAR \| SHORT INT INTEGER LONG OBJECT NOT NULL \| TEMPORARY \| \| \| \[ \] \[ \] \[ LOCALIZABLE \] \[ HOLD \] .<br/>                                                                                                                                                                  |
| Mantener y liberar tablas temporales     | ALTER TABLE {table name} HOLDALTER TABLE {table name} FREE<br/> El usuario puede usar los comandos HOLD y FREE para controlar el intervalo de vida de una tabla temporal o una columna temporal. El recuento de retención en una tabla se incrementa para cada operación HOLD SQL en esa tabla y se disminuye para cada operación FREE SQL en la tabla. Cuando se libera el último recuento de retenciones en una tabla, todas las columnas temporales se vuelven inaccesibles. Si todas las columnas son temporales, la tabla pasa a ser inaccesible.<br/>     |



 

Para obtener más información, vea [Ejemplos de consultas de base de](examples-of-database-queries-using-sql-and-script.md)datos SQL y Script .

### <a name="sql-grammar"></a>Gramática de SQL

Los parámetros opcionales se muestran entre \[ \] corchetes. Cuando se muestran varias opciones, los parámetros opcionales se separan mediante una barra vertical.

{constant} es una cadena o un entero. Una cadena debe incluirse entre comillas simples 'example'. {constant-list} es una lista delimitada por comas de una o varias constantes.

La opción LOCALIZABLE establece un atributo de columna que indica que la columna debe localizarse.

{column} es una referencia en columnas a un valor de un campo de una tabla.

{marker} es una referencia de parámetro a un valor proporcionado por un registro enviado con la consulta. Se representa en la instrucción SQL mediante un signo de interrogación ?. Para obtener información sobre el uso de parámetros, vea la [**función MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) o [**el método Execute.**](view-execute.md)

La Windows installer SQL no admite el escape de comillas simples (valor ASCII 39) en un literal de cadena. Sin embargo, puede capturar o crear el registro, establecer el campo con la [**propiedad StringData**](record-stringdata.md) o [**IntegerData**](record-integerdata.md) y, a continuación, llamar [**al método Modify.**](view-modify.md) Como alternativa, puede crear un registro y usar los marcadores de parámetro (?) que se describen en [**Método Execute.**](view-execute.md) También puede hacerlo mediante las funciones de base de datos [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute), [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)y [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa).

Una cláusula WHERE {operation-list} es opcional y es una agrupación de operaciones que se usarán para filtrar la selección. Las operaciones deben ser de los siguientes tipos:

-   {column} = {column}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {constant}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {marker}
-   {column} es null
-   {column} no es null

En el caso de los valores de cadena, solo se pueden realizar <> operaciones . Las comparaciones de valores de objeto se limitan a IS NULL y IS NOT NULL.

Las operaciones individuales se pueden agrupar por operadores AND u OR. La ordenación se puede imponer mediante el uso de paréntesis ( ).

La cláusula ORDER BY es opcional y provoca un retraso inicial durante la ordenación. La ordenación por cadenas agrupará cadenas idénticas, pero no las ordenará alfabéticamente.

La cláusula DISTINCT es opcional y no repite registros idénticos en el conjunto de resultados devuelto.

{table-list} es una lista delimitada por comas de uno o varios nombres de tabla a los que se hace referencia como {table} en la combinación.

{column-list} es una lista delimitada por comas de una o varias columnas de tabla denominadas {column} seleccionadas. Las columnas ambiguas se pueden calificar aún más como {tablename.column}. Se puede usar un asterisco como lista de columnas en una consulta SELECT para representar todas las columnas de las tablas a las que se hace referencia. Al hacer referencia a campos por posición de columna, seleccione las columnas por nombre en lugar de usar el asterisco. No se puede usar un asterisco como una lista de columnas en una consulta INSERT INTO.

Para escapar nombres de tabla y nombres de columna que entren en conflicto SQL palabras clave, incluya el nombre entre dos acentos graves \` \` (valor ASCII 96). Si un nombre de columna debe tener caracteres de escape y está calificado como {tablename.column}, la tabla y la columna se deben escapar individualmente como { \` tablename \` . \` columna \` }. Se recomienda que todos los nombres de tabla y de columna se escapen de esta manera para evitar conflictos con palabras reservadas y obtener un rendimiento significativo.

Los nombres de tabla están limitados a 31 caracteres. Para obtener más información, vea [Nombres de tabla](table-names.md). Los nombres de tabla y columna distinguen mayúsculas de minúsculas. SQL palabras clave no distinguen mayúsculas de minúsculas.

El número máximo de expresiones en una cláusula WHERE de una SQL consulta está limitado a 32.

Solo se admiten combinaciones internas y se especifican mediante una comparación de columnas de tablas diferentes. No se admiten combinaciones circulares. Una combinación circular es una SQL consulta que vincula tres o más tablas a un circuito. Por ejemplo, lo siguiente es una combinación circular:

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

Las columnas que forman parte de las claves principales de una tabla deben definirse primero en orden de prioridad, seguido de cualquier columna de clave no primaria. Las columnas persistentes deben definirse antes que las columnas temporales. La secuencia de ordenación de una columna de texto no está definida; Sin embargo, los valores de texto idénticos siempre se agrupan.

Tenga en cuenta que al agregar o crear una columna, debe especificar el tipo de columna.

Las tablas no pueden contener más de una columna de tipo 'object'.

El tamaño máximo que se puede especificar explícitamente para una columna de cadena en una consulta SQL es 255. Una columna de cadena de longitud infinita se representa como con el tamaño 0. Para obtener más información, vea [Formato de definición de columna](column-definition-format.md).

Para ejecutar cualquier instrucción SQL, se debe crear una vista. Sin embargo, una vista que no crea un conjunto de resultados, como CREATE TABLE o INSERT INTO, no se puede usar con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o el método [**Modify**](view-modify.md) para actualizar tablas a través de la vista.

Tenga en cuenta que no puede capturar un registro que contenga datos binarios de una base de datos y, a continuación, usar ese registro para insertar los datos en una base de datos completamente diferente. Para mover datos binarios de una base de datos a otra, debe exportar los datos a un archivo y, a continuación, importarlos en la nueva base de datos a través de una consulta y la [**función MsiRecordSetStream.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) Esto garantiza que cada base de datos tenga su propia copia de los datos binarios.

 

 




