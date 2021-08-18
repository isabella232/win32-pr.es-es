---
description: 'Más información sobre: JetSetColumn (Función)'
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
ms.openlocfilehash: 848d575f6fd8598aa3262273e9da3ce4cd1aaed12bcb2dc17e41e0d2f98bfdad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978865"
---
# <a name="jetsetcolumn-function"></a>Función JetSetColumn


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetcolumn-function"></a>Función JetSetColumn

La **función JetSetColumn** modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual. Puede sobrescribir un valor existente, agregar un nuevo valor a una secuencia de valores de una columna con varios valores, quitar un valor de una secuencia de valores de una columna de varios valores o actualizar todo o parte de un valor largo, una columna de tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md).

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

*tableid*

Cursor que se va a usar para esta llamada.

*columnid*

El [JET_COLUMNID](./jet-columnid.md) de la columna que se va a recuperar. Como alternativa, se puede especificar un valor de *columnid* de 0 (cero). Cuando *se da columnid* 0 (cero), todas las columnas etiquetadas, columnas dispersas y con varios valores, se tratan como una sola columna. Esto facilita la recuperación de todas las columnas dispersas que están presentes en un registro.

*pvData*

Búfer de entrada que contiene los datos que se usarán para el valor de columna.

*cbData*

Tamaño en bytes del búfer de entrada.

*grbit*

Un grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Esta opción se usa para anexar datos a una columna de <a href="gg269213(v=exchg.10).md">tipo JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. El mismo comportamiento se puede lograr determinando el tamaño del valor long existente y especificando <em>ibLongValue</em> en <em>psetinfo</em>. Sin embargo, es más sencillo usar este <em>grbit,</em> ya que no es necesario conocer el tamaño del valor de columna existente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Esta opción se usa para reemplazar el valor long existente por los datos recién proporcionados. Cuando se usa esta opción, es como si el valor long existente se hubiera establecido en 0 (cero) longitud antes de establecer los nuevos datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Esta opción solo es aplicable a las columnas etiquetadas, dispersas o con varios valores. Hace que la columna devuelva el valor de columna predeterminado en las operaciones de recuperación de columnas posteriores. Se quitan todos los valores de columna existentes.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Esta opción se usa para forzar que un valor largo, las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, se almacenen por separado del resto de datos de registro. Esto sucede normalmente cuando el tamaño del valor largo impide que se almacene con los datos de registro restantes. Sin embargo, esta opción se puede usar para forzar que el valor long se almacene por separado. Tenga en cuenta que no se puede forzar la separación de los valores largos de cuatro bytes de tamaño menor. En tales casos, se omite la opción .</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Esta opción se usa para interpretar el búfer de entrada como un número entero de bytes para establecer como la longitud del valor largo descrito por el <em>columnid</em> especificado y, si se proporciona, el número de secuencia en psetinfo- &gt; itagSequence. Si el tamaño especificado es mayor que el valor de columna existente, la columna se ampliará con 0s. Si el tamaño es menor que el valor de columna existente, el valor se truncará.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Esta opción se usa para exigir que todos los valores de una columna con varios valores sean distintos. Esta opción compara los datos de la columna de origen, sin ninguna transformación, con otros valores de columna existentes y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, JET_bitSetAppendLV, JET_bitSetOverwriteLV y JET_bitSetSizeLV también se pueden proporcionar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Esta opción se usa para exigir que todos los valores de una columna con varios valores sean distintos. Esta opción compara la transformación normalizada de clave de los datos de columna con otros valores de columna existentes transformados de forma similar y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, JET_bitSetAppendLV, JET_bitSetOverwriteLV y JET_bitSetSizeLV también se pueden proporcionar.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Esta opción se usa para establecer un valor en longitud cero. Normalmente, un valor de columna se establece <strong>en NULL</strong> pasando cbMax de 0 (cero). Sin embargo, para algunos tipos, <a href="gg269213(v=exchg.10).md">como JET_coltypText</a>, un valor de columna puede tener una longitud <strong></strong> de 0 (cero) en lugar de <strong>NULL</strong>y esta opción se usa para diferenciar entre null y 0 (cero) longitud.</p>
<p><strong>Nota</strong>  En general, si la columna es una columna de longitud fija, este bit se omite y la columna se establece en <strong>NULL.</strong> Sin embargo, si la columna es una columna etiquetada de longitud fija, la longitud de la columna se establece en 0. Cuando la columna etiquetada de longitud fija se establece en 0 longitud, los intentos de recuperar la columna con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> se realizarán correctamente, pero la longitud real que se devuelve en el <em>parámetro cbActual</em> es 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Esta opción se usa para almacenar todo el valor largo en el registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetCompressed</p></td>
<td><p>Esta opción se usa para intentar la compresión de datos al almacenar los datos.</p>
<p><strong>Windows 7:</strong>  JET_bitSetCompressed se introdujo en Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUncompressed</p></td>
<td><p>Esta opción no se usa para intentar la compresión al almacenar los datos.</p>
<p><strong>Windows 7:</strong>  JET_bitSetUnCompressed se introdujo en Windows 7.</p></td>
</tr>
</tbody>
</table>


*psetinfo*

Puntero a parámetros de entrada opcionales que se pueden establecer para esta función mediante la [JET_SETINFO](./jet-setinfo-structure.md) estructura.

Si *psetinfo* se especifica como **NULL,** la función se comporta como si se hubieran dado una *itagSequence* de 1 y *un valor ibLongValue* de 0 (cero). Esto hace que el conjunto de columnas establezca el primer valor de una columna con varios valores y que establezca datos largos a partir del desplazamiento 0 (cero).

Se pueden establecer las siguientes opciones para este parámetro:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
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
<td><p>Número de secuencia del valor de columna multivalor deseado que se establecerá. Si <em>itagSequence</em> se establece en 0 (cero), el valor proporcionado se debe anexar al final de la secuencia de valores multivalor. Si el número de secuencia proporcionado es mayor que el último valor multivalor existente, se anexa de nuevo el valor especificado al final de la secuencia de valores. Si el número de secuencia corresponde a un valor existente, ese valor se reemplaza por el valor especificado.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>El identificador de columna especificado está fuera de los límites legales de un identificador de columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La columna descrita por el <em>columnid</em> dado no existe en la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable</p></td>
<td><p>Se intentó actualizar un valor largo durante una operación de actualización original de eliminación de copia de inserción.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig</p></td>
<td><p>Los datos de valor de columna especificados en el búfer de entrada superan la limitación de tamaño natural para una columna de longitud fija o están configurados para columnas binarias o de texto de longitud fija. Este error también se devuelve cuando se pasan más de 1024 bytes de datos para una columna larga y se establece la marca JET_bitSetIntrinsicLV datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>El tamaño de datos del valor de columna especificado no coincide con lo que es natural para el tipo de datos de longitud fija.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Se intentó actualizar una columna de incremento automático durante una operación de inserción o actualización, o bien actualizar una columna de versión durante una operación de reemplazo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Las opciones proporcionadas son desconocidas o una combinación no conocida de la configuración de bits conocida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>El psetinfo- &gt; cbStruct especificado no es un tamaño válido para la <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> estructura.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate</p></td>
<td><p>La operación de establecer columna intentó crear un valor duplicado y especificó JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Se intentó actualizar un valor de columna largo cuando la sesión de llamada no estaba en una transacción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Se intentó establecer una columna que no es<strong>NULL</strong> en <strong>NULL.</strong></p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Igual que JET_errNullInvalid.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>El valor de columna no se pudo establecer en el valor del búfer de entrada porque habría hecho que el registro superara su limitación de tamaño de página relacionada. Las columnas de <a href="gg269213(v=exchg.10).md">tipo JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> pueden almacenarse por separado de los datos de registro restantes. Sin embargo, otras columnas deben almacenarse con el registro y pueden hacer que se supere la limitación de tamaño del registro. Incluso las columnas largas requieren 5 bytes de espacio dentro del registro como vinculación y esto también puede provocar que JET_errRecordTooBig se devuelvan.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>El cursor no está actualmente en proceso de insertar un nuevo registro o de actualizar uno existente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Este error se producirá cuando el tamaño configurado del almacén de versiones no sea suficiente para contener todas las actualizaciones pendientes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>El valor de columna del búfer de entrada superó la longitud máxima configurada para una columna de longitud variable y se truncó.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, la parte deseada de un valor de columna para la columna especificada se establece con los datos copiados del búfer de entrada. Es posible que el conjunto de datos se haya truncado si ha superado la longitud máxima especificada para una columna de longitud variable.

En caso de error, la ubicación del cursor se deja sin cambios y no se actualizan datos de valor de columna en el búfer de copia.

#### <a name="remarks"></a>Comentarios

Establecer valores largos, valores para columnas [JET_coltypLongBinary](./jet-coltyp.md) de tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md), solo se deben realizar cuando la sesión de llamada está en una transacción. Si la sesión de llamada no está en una transacción, las modificaciones en los valores largos que se almacenan por separado pueden estar totalmente confirmadas incluso cuando la operación de actualización se cancele más adelante. Si la sesión de llamada está en una transacción, los efectos de la actualización se pueden revertir completamente cancelando la actualización y revierte la transacción de sesión.

Las actualizaciones de índice no se realizan como resultado de **las operaciones de JetSetColumn.** En su lugar, los índices solo se actualizan una vez completadas todas las modificaciones de columna [y se llama a JetUpdate.](./jetupdate-function.md) Esto permite la actualización más eficaz de los índices cuando los índices implican la modificación de más de una columna.

Un registro tiene un tamaño limitado en función del tamaño de página de la base de datos. Los valores largos del registro de más de cinco bytes se almacenarán separados del registro en caso de que los datos del registro superen su límite como resultado de una **operación JetSetColumn.** El error JET_errRecordTooBig solo se devolverá después de que todos los datos de la columna de registro separable se hayan almacenado por separado del registro y el registro supere el límite de tamaño del registro.

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
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
