---
description: 'Más información acerca de: JetSetColumn (función)'
title: Función JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705745"
---
# <a name="jetsetcolumn-function"></a>Función JetSetColumn


_**Se aplica a:** Windows | Windows Server_

## <a name="jetsetcolumn-function"></a>Función JetSetColumn

La función **JetSetColumn** modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual. Puede sobrescribir un valor existente, agregar un nuevo valor a una secuencia de valores en una columna con varios valores, quitar un valor de una secuencia de valores de una columna con varios valores o actualizar todo o parte de un valor Long, una columna de tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md).

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*columnid*

[JET_COLUMNID](./jet-columnid.md) de la columna que se va a recuperar. Como alternativa, se puede proporcionar un valor de *columnid* de 0 (cero). Cuando se proporciona *columnid* 0 (cero), todas las columnas etiquetadas, las columnas dispersas y con varios valores, se tratan como una sola columna. Esto facilita la recuperación de todas las columnas dispersas que se encuentran en un registro.

*pvData*

Búfer de entrada que contiene los datos que se van a usar para el valor de columna.

*cbData*

Tamaño en bytes del búfer de entrada.

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Esta opción se utiliza para anexar datos a una columna de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. Se puede lograr el mismo comportamiento determinando el tamaño del valor Long existente y especificando <em>ibLongValue</em> en <em>psetinfo</em>. Sin embargo, es más fácil usar esta <em>grbit</em> , ya que no es necesario conocer el tamaño del valor de la columna existente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Esta opción se usa para reemplazar el valor Long existente con los datos proporcionados recientemente. Cuando se usa esta opción, es como si el valor Long existente se hubiera establecido en la longitud 0 (cero) antes de establecer los datos nuevos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Esta opción solo es aplicable para columnas etiquetadas, dispersas o con varios valores. Hace que la columna devuelva el valor de columna predeterminado en operaciones de recuperación de columna posteriores. Se quitan todos los valores de columna existentes.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Esta opción se usa para forzar un valor largo, columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, que se almacenarán por separado del resto de datos de registro. Esto ocurre normalmente cuando el tamaño del valor Long impide que se almacene con los datos de registro restantes. Sin embargo, esta opción se puede usar para forzar el almacenamiento del valor largo por separado. Tenga en cuenta que no se puede forzar la separación de los valores Long de cuatro bytes de menor tamaño. En estos casos, se omite la opción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Esta opción se usa para interpretar el búfer de entrada como un número entero de bytes que se establecerá como la longitud del valor largo descrito por el <em>columnid</em> determinado y, si se proporciona, el número de secuencia en psetinfo- &gt; itagSequence. Si el tamaño dado es mayor que el valor de columna existente, la columna se extenderá con 0s. Si el tamaño es menor que el valor de la columna existente, el valor se truncará.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Esta opción se utiliza para exigir que todos los valores de una columna con varios valores sean distintos. Esta opción compara los datos de la columna de origen, sin ninguna transformación, con otros valores de columna existentes y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, no se pueden proporcionar también JET_bitSetAppendLV, JET_bitSetOverwriteLV y JET_bitSetSizeLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Esta opción se utiliza para exigir que todos los valores de una columna con varios valores sean distintos. Esta opción compara la transformación normalizada clave de datos de columna con otros valores de columna existentes transformados de forma similar y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, no se pueden proporcionar también JET_bitSetAppendLV, JET_bitSetOverwriteLV y JET_bitSetSizeLV.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Esta opción se usa para establecer un valor de longitud cero. Normalmente, un valor de columna se establece en <strong>null</strong> pasando un cbMax de 0 (cero). Sin embargo, para algunos tipos, como <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valor de columna puede ser una longitud de 0 (cero) en lugar de <strong>null</strong>, y esta opción se usa para diferenciar entre la longitud <strong>null</strong> y 0 (cero).</p>
<p><strong>Nota:</strong>  En general, si la columna es una columna de longitud fija, este bit se omite y la columna se establece en <strong>null</strong>. Sin embargo, si la columna es una columna etiquetada de longitud fija, la longitud de la columna se establece en 0. Cuando la columna etiquetada de longitud fija está establecida en una longitud de 0, los intentos de recuperar la columna con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> se realizarán correctamente, pero la longitud real que se devuelve en el parámetro <em>cbActual</em> es 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Esta opción se usa para almacenar el valor largo completo en el registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetCompressed</p></td>
<td><p>Esta opción se utiliza para intentar la compresión de datos al almacenar los datos.</p>
<p><strong>Windows 7:</strong>  JET_bitSetCompressed se presenta en Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUncompressed</p></td>
<td><p>Esta opción se usa para no intentar la compresión al almacenar los datos.</p>
<p><strong>Windows 7:</strong>  JET_bitSetUnCompressed se presenta en Windows 7.</p></td>
</tr>
</tbody>
</table>


*psetinfo*

Puntero a los parámetros de entrada opcionales que se pueden establecer para esta función mediante la estructura [JET_SETINFO](./jet-setinfo-structure.md) .

Si *psetinfo* se proporciona como **null** , la función se comporta como si se hubiera especificado un valor de *itagSequence* de 1 y un valor de *ibLongValue* de 0 (cero). Esto hace que el conjunto de columnas establezca el primer valor de una columna con varios valores y que se establezcan datos largos a partir del desplazamiento 0 (cero).

Se pueden establecer las siguientes opciones para este parámetro:

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
<td><p>Desplazamiento binario en un valor de columna largo donde deben comenzar los datos establecidos.</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>Número de secuencia del valor de columna multivalor deseado que se va a establecer. Si <em>itagSequence</em> se establece en 0 (cero), el valor proporcionado debe anexarse al final de la secuencia de valores multivalor. Si el número de secuencia proporcionado es mayor que el último valor de varios valores existente, el valor especificado se anexa al final de la secuencia de valores. Si el número de secuencia corresponde a un valor existente, ese valor se reemplaza por el valor especificado.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La columna descrita por el <em>columnid</em> determinado no existe en la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable</p></td>
<td><p>Se intentó actualizar un valor Long durante una operación de eliminación de la actualización original.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig</p></td>
<td><p>Los datos de los valores de columna especificados en el búfer de entrada superan el límite de tamaño, ya sea natural para una columna de longitud fija o configurados para columnas binarias o de texto de longitud fija. Este error también se devuelve al pasar más de 1024 bytes de datos para una columna larga y al establecer la marca de JET_bitSetIntrinsicLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>El tamaño de los datos del valor de la columna dado no coincide con el tipo de datos de longitud fija.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Se realizó un intento no válido de actualizar una columna de incremento automático durante una operación de inserción o actualización, o bien para actualizar una columna de versión durante una operación de reemplazo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Las opciones proporcionadas son desconocidas o una combinación no válida de valores de bits conocidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>El psetinfo especificado- &gt; cbStruct no es un tamaño válido para la estructura de <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate</p></td>
<td><p>La operación establecer columna intentó crear un valor duplicado y especificó JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Se intentó actualizar un valor de columna largo cuando la sesión que realiza la llamada no se encontraba en una transacción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Se hizo un intento no válido de establecer una columna que no es<strong>null</strong> en <strong>null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Igual que JET_errNullInvalid.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>No se pudo establecer el valor de la columna en el valor del búfer de entrada porque habría hecho que el registro superara su límite de tamaño de página relacionado. Las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> pueden almacenarse independientemente de los datos de registro restantes. Sin embargo, otras columnas deben almacenarse con el registro y pueden provocar que se supere la limitación del tamaño del registro. Las columnas de tipo Long requieren 5 bytes de espacio en el registro como una vinculación y esto puede provocar que se devuelva JET_errRecordTooBig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>El cursor no está actualmente en proceso de insertar un nuevo registro o actualizar un registro existente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Este error se producirá cuando el tamaño configurado del almacén de versiones no sea suficiente para contener todas las actualizaciones pendientes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>El valor de la columna en el búfer de entrada superó la longitud máxima configurada para una columna de longitud variable y se truncó.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, la parte deseada de un valor de columna para la columna especificada se establece con los datos copiados desde el búfer de entrada. Es posible que se haya truncado el conjunto de datos si ha superado la longitud máxima especificada para una columna de longitud variable.

En caso de error, la ubicación del cursor permanece sin cambios y no se actualiza ningún dato del valor de columna en el búfer de copia.

#### <a name="remarks"></a>Observaciones

Establecer valores Long, los valores de las columnas [JET_coltypLongBinary](./jet-coltyp.md) de tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md), debe realizarse solo cuando la sesión de llamada está en una transacción. Si la sesión que realiza la llamada no está en una transacción, las modificaciones realizadas en valores largos que se almacenan por separado se pueden confirmar por completo incluso cuando se cancela la operación de actualización posteriormente. Si la sesión que realiza la llamada está en una transacción, los efectos de la actualización se pueden revertir por completo cancelando la actualización y revirtiendo la transacción de la sesión.

No se realizan actualizaciones de índice como resultado de las operaciones de **JetSetColumn** . En su lugar, los índices solo se actualizan una vez completadas todas las modificaciones de las columnas y se llama a [JetUpdate](./jetupdate-function.md) . Esto permite la actualización más eficaz de los índices cuando los índices implican que se está modificando más de una columna.

Un registro tiene un tamaño limitado según el tamaño de la página de la base de datos. Los valores largos del registro de más de cinco bytes se almacenarán por separado del registro en caso de que los datos del registro superen su límite como resultado de una operación **JetSetColumn** . El JET_errRecordTooBig de error solo se devolverá después de que todos los datos de columna de registro separables se hayan almacenado por separado del registro y el registro supere el límite de tamaño del registro.

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
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
