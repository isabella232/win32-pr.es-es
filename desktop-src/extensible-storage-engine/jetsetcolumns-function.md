---
description: 'Más información acerca de: JetSetColumns (función)'
title: Función JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153767"
---
# <a name="jetsetcolumns-function"></a>Función JetSetColumns


_**Se aplica a:** Windows | Windows Server_

## <a name="jetsetcolumns-function"></a>Función JetSetColumns

La función **JetSetColumns** tiene un comportamiento similar al de [JetSetColumn](./jetsetcolumn-function.md) , pero permite que una aplicación establezca varios valores de columna en una sola operación. Una matriz de estructuras [JET_SETCOLUMN](./jet-setcolumn-structure.md) se utiliza para describir el conjunto de valores de columna que se va a establecer y para describir los búferes de entrada de cada valor de columna que se va a establecer.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*psetcolumn*

Puntero a una matriz de una o varias estructuras de [JET_SETCOLUMN](./jet-setcolumn-structure.md) . Cada estructura incluye descripciones de los valores de columna que se van a establecer y desde dónde obtener los datos de columna que se van a establecer.

*csetcolumn*

El número de estructuras [JET_SETCOLUMN](./jet-setcolumn-structure.md) en la matriz dada por *psetcolumn*.

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
<td><p>JET_errBadColumnId</p></td>
<td><p>El ID. de columna especificado está fuera de los límites legales de un identificador de columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Igual que JET_errNullInvalid.</p></td>
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
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
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
<td><p>Se hizo un intento no válido de establecer una columna que no es NULL en NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>No se pudo establecer el valor de la columna en el valor del búfer de entrada porque habría hecho que el registro superara su límite de tamaño de página relacionado. Las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> pueden almacenarse independientemente de los datos de registro restantes. Sin embargo, otras columnas deben almacenarse con el registro y pueden provocar que se supere la limitación del tamaño del registro. Las columnas de tipo Long requieren 5 bytes de espacio en el registro como una vinculación y esto puede provocar que se devuelva JET_errRecordTooBig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>El cursor no está actualmente en proceso de insertar un nuevo registro o actualizar un registro existente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>El valor de la columna en el búfer de entrada superó la longitud máxima configurada para una columna de longitud variable y se truncó.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, para cada columna descrita en psetcolumns, la parte deseada del valor de la columna se establece con datos copiados desde el búfer de entrada. Es posible que se haya truncado el conjunto de datos de la columna si se superó la longitud máxima especificada para una columna de longitud variable.

En caso de error, la ubicación del cursor permanece sin cambios y no se actualiza ningún dato del valor de columna en el búfer de copia.

#### <a name="remarks"></a>Observaciones

Si alguna operación individual de una columna devuelve un error, la operación **JetSetColumns** completa devolverá un error. En general, las advertencias se devuelven en psetcolumns- \> error y no en el código de retorno de esta función. Sin embargo, si el último conjunto de columnas tiene una advertencia, esta advertencia se devolverá desde **JetSetColumns** .

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
