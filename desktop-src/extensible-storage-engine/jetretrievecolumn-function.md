---
description: 'Más información acerca de: JetRetrieveColumn (función)'
title: Función JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707179"
---
# <a name="jetretrievecolumn-function"></a>Función JetRetrieveColumn


_**Se aplica a:** Windows | Windows Server_

## <a name="jetretrievecolumn-function"></a>Función JetRetrieveColumn

La función **JetRetrieveColumn** recupera un valor de columna único del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor. Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor. Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual. Además de recuperar el valor de la columna real, **JetRetrieveColumn** también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*columnid*

[JET_COLUMNID](./jet-columnid.md) de la columna que se va a recuperar.

Se puede proporcionar un valor de *columnid* de 0 (cero) que no hace referencia a ninguna columna individual. Cuando se proporciona *columnid* 0 (cero), todas las columnas etiquetadas, dispersas y columnas con varios valores se tratan como una sola columna. Esto facilita la recuperación de todas las columnas dispersas que se encuentran en un registro.

*pvData*

Búfer de salida que recibe el valor de la columna.

*cbData*

Tamaño máximo, en bytes, del búfer de salida.

*pcbActual*

Recibe el tamaño real, en bytes, del valor de la columna.

Si este parámetro es **null**, no se devolverá el tamaño real del valor de la columna.

*grbit*

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Esta marca hace que la columna de recuperación recupere el valor modificado en lugar del valor original. Si el valor no se ha modificado, se recupera el valor original. De esta manera, se puede recuperar un valor que todavía no se ha insertado o actualizado durante la operación de inserción o actualización de un registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>Esta opción se utiliza para recuperar los valores de columna del índice, si es posible, sin tener acceso al registro. De esta manera, se puede evitar la carga innecesaria de registros cuando los datos necesarios están disponibles en las propias entradas de índice. En los casos en los que no se puede recuperar el valor de la columna original del índice debido a las transformaciones irreversibles o al truncamiento de los datos, se obtendrá acceso al registro y se recuperarán los datos de la forma habitual. Se trata de una opción de rendimiento y solo se debe especificar cuando es probable que se pueda recuperar el valor de la columna del índice. Esta opción no se debe especificar si el índice actual es el índice clúster, ya que las entradas de índice para el índice agrupado, o principal, son los propios registros. No se puede establecer este bit si también se establece JET_bitRetrieveFromPrimaryBookmark.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>Esta opción se usa para recuperar valores de columna del marcador de índice y puede diferir del valor de índice cuando una columna aparece en el índice principal y en el índice actual. Esta opción no se debe especificar si el índice actual es el índice clúster o principal. No se puede establecer este bit si también se establece JET_bitRetrieveFromIndex.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>Esta opción se usa para recuperar el número de secuencia de un valor de columna de varios valores en pretinfo- &gt; itagSequence. El campo itagSequence suele ser una entrada para recuperar valores de columna con varios valores de un registro. Sin embargo, cuando se recuperan valores de un índice, también es posible asociar la entrada de índice con un número de secuencia determinado y recuperar también este número de secuencia. Recuperar el número de secuencia puede ser una operación costosa y solo debe realizarse si es necesario.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveNull</p></td>
<td><p>Esta opción se usa para recuperar los valores <strong>null</strong> de las columnas con varios valores. Si no se especifica esta opción, se omitirán automáticamente los valores <strong>null</strong> de las columnas con varios valores.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>Esta opción solo afecta a las columnas con varios valores y hace que se devuelva un valor <strong>null</strong> cuando el número de secuencia solicitado es 1 y no hay valores establecidos para la columna en el registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>Esta marca solo es para uso interno y no está pensada para usarse en la aplicación.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>Esta marca solo es para uso interno y no está pensada para usarse en la aplicación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveTuple</p></td>
<td><p>Esta marca permitirá la recuperación de un segmento de tupla del índice. Este bit debe especificarse con JET_bitRetrieveFromIndex.</p></td>
</tr>
</tbody>
</table>


*pretinfo*

Si *pretinfo* se da como **null** , la función se comporta como si se hubiera proporcionado un valor de *ItagSequence* de 1 y una *ibLongValue* de 0 (cero). Esto hace que la recuperación de columnas recupere el primer valor de una columna con varios valores y que recupere datos largos en el desplazamiento 0 (cero).

Este parámetro se usa para proporcionar uno o varios de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ibLongValue</p></td>
<td><p>Proporciona un desplazamiento binario en un valor de columna largo cuando se recupera una parte del valor de una columna.</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>Proporciona el número de secuencia del valor de columna de varios valores deseado. Tenga en cuenta que este campo solo se establece si se especifica el JET_bitRetrieveTag. De lo contrario, no se modifica.</p></td>
</tr>
<tr class="odd">
<td><p>columnidNextTagged</p></td>
<td><p>Devuelve el ID. de columna del valor de la columna devuelta cuando se recuperan todas las columnas etiquetadas, dispersas y con varios valores, mediante el paso de <em>columnid</em> de 0 (cero).</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadColumnId</p></td>
<td><p>El ID. de columna especificado está fuera de los límites legales de un identificador de columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadItagSequence</p></td>
<td><p>Se pasó un valor de número de secuencia de columna con varios valores no válido en pretinfo- &gt; itagSequence. Los valores válidos para los números de secuencia de valores de columna con varios valores son 1 o superior. Un valor de 0 (cero) no es válido para esta función.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La columna descrita por el <em>columnid</em> determinado no existe en la tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex</p></td>
<td><p>Las columnas indizadas como subcadenas no se pueden recuperar del índice, puesto que solo una pequeña parte de la columna está presente normalmente en cada entrada de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>En algunos casos, el búfer proporcionado para la columna de recuperación debe tener el tamaño suficiente para poder devolver cualquier cantidad de valor de columna. Por ejemplo, las columnas actualizables de custodia se ajustan para ser coherentes con el contexto transaccional de la sesión de llamada y este ajuste requiere el búfer proporcionado por el autor de la llamada. Si se proporciona espacio en búfer insuficiente, se devuelve JET_errInvalidBufferSize y no se devuelve ningún dato de columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno o varios de los parámetros especificados no son correctos. Esto puede ocurrir si retinfo. cbStruct es más pequeño que el tamaño de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Las opciones proporcionadas son desconocidas o una combinación no válida de valores de bits conocidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está situado en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>No se pudo recuperar el valor de columna completo porque el búfer especificado es menor que el tamaño de la columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>El valor de columna recuperado es <strong>null</strong>.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el valor de columna de la columna especificada se copia en el búfer especificado. Se copia un valor menor que el de la columna con la advertencia JET_wrnBufferTruncated se devuelve. Si se proporciona *pcbActual* , se devuelve el tamaño real del valor de la columna. Tenga en cuenta que los valores **null** tienen una longitud de 0 (cero) y, por tanto, establecerán el tamaño devuelto en 0 (cero). Si la columna recuperada era una columna con varios valores y se ha especificado *pretinfo* , y JET_bitReturnTag se estableció como una opción, el número de secuencia del valor de la columna se devuelve en pretinfo- \> itagSequence.

En caso de error, la ubicación del cursor se deja sin modificar y no se copia ningún dato en el búfer proporcionado.

#### <a name="remarks"></a>Observaciones

Esta llamada se usa solo una vez para recuperar datos de tamaño fijo o conocido para las columnas que no son de varios valores. Sin embargo, cuando los datos de columna tienen un tamaño desconocido, esta llamada se usa normalmente dos veces. Se llama primero para determinar el tamaño de los datos para que pueda asignar el espacio de almacenamiento necesario. A continuación, se vuelve a realizar la misma llamada para recuperar los datos de la columna. Cuando se desconoce el número real de valores, ya que una columna tiene varios valores, normalmente se usa la llamada tres veces. En primer lugar, obtenga el número de valores y, a continuación, dos veces más para asignar el almacenamiento y recuperar los datos reales.

Para recuperar todos los valores de una columna con varios valores, se puede realizar una llamada repetida a esta función con un valor de pretinfo- \> itagSequence a partir de 1 y aumentar en cada llamada subsiguiente. Se sabe que el último valor de la columna se recupera cuando se devuelve un JET_wrnColumnNull de la función. Tenga en cuenta que este método no se puede hacer si la columna de varios valores tiene valores **null** explícitos establecidos en su secuencia de valores, ya que estos valores se omitirán. Si una aplicación desea recuperar todos los valores de columna con varios valores, incluidos los que se establecen explícitamente en **null**, se debe usar [JetRetrieveColumns](./jetretrievecolumns-function.md) en lugar de **JetRetrieveColumn**. Tenga en cuenta que esta función no devuelve el número de valores para una función con varios valores cuando se proporciona un valor de *itagSequence* de 0 (cero). Solo [JetRetrieveColumns](./jetretrievecolumns-function.md) devolverá el número de valores de un valor de columna cuando se pasa un valor de *itagSequence* de 0 (cero).

Si se llama a esta función en el nivel de transacción 0 (cero), por ejemplo, la sesión que realiza la llamada no se realiza en una transacción, se abre y se cierra una transacción dentro de la función. El propósito de esto es devolver resultados coherentes en caso de que un valor Long abarque páginas de base de datos. Tenga en cuenta que la transacción se libera entre las llamadas de función y una serie de llamadas a esta función cuando la sesión no está en una transacción puede devolver datos actualizados después de la primera llamada a esta función.

Se recuperará el valor predeterminado de la columna cuando la columna no se haya establecido explícitamente en otro valor, a menos que se establezca la opción JET_bitRetrieveIgnoreDefault.

Recuperar el valor de la columna AutoIncrement del búfer de copia antes de la inserción es un medio común para identificar un registro de forma exclusiva para la vinculación al insertar datos normalizados en varias tablas. El valor de incremento automático se asigna cuando se inicia la operación de inserción y se puede recuperar del búfer de copia en cualquier momento hasta que se complete la actualización.

Cuando se recuperan todas las columnas etiquetadas, con varios valores y dispersas, al establecer *columnid* en 0 (cero), las columnas se recuperan en orden *columnid* desde el valor de *columnid* más bajo a *columnid* superior. Se devuelve el mismo orden de valores de columna cada vez que se recuperan los valores de columna. El orden es determinista.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JetSetColumn](./jetretrievekey-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
