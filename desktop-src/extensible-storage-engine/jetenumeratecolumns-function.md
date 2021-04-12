---
description: 'Más información acerca de: JetEnumerateColumns (función)'
title: Función JetEnumerateColumns
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277859"
---
# <a name="jetenumeratecolumns-function"></a>Función JetEnumerateColumns


_**Se aplica a:** Windows | Windows Server_

## <a name="jetenumeratecolumns-function"></a>Función JetEnumerateColumns

La función **JetEnumerateColumns** recupera eficazmente un conjunto de columnas y sus valores del registro actual de un cursor o del búfer de copia de ese cursor. Las columnas y los valores recuperados se pueden restringir por una lista de identificadores de columna, números de *itagSequence* y otras características. Esta API de recuperación de columnas es única, ya que devuelve información en memoria asignada dinámicamente que se obtiene mediante una devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) proporcionada por el usuario. Esta nueva flexibilidad permite la recuperación eficaz de datos de columna con características específicas (como el tamaño y la multiplicidad) que son desconocidas para el autor de la llamada. Esto elimina la necesidad de usar los modos de detección de [JetRetrieveColumn](./jetretrievecolumn-function.md) para determinar esas características a fin de configurar una llamada final a [JetRetrieveColumn](./jetretrievecolumn-function.md) que recupere correctamente los datos deseados.

**Windows XP: JetEnumerateColumns** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*cEnumColumnId*

Una matriz de identificadores de columna, cada uno con una matriz opcional de números *itagSequence* para enumerar.

Si *cEnumColumnId* es 0 (cero), *rgEnumColumnId* se omite y todos los valores de columna se enumeran y se devuelven al autor de la llamada. Si un elemento de la matriz de ID. de columna hace referencia a un ID. de columna de 0 (cero), se omitirá la enumeración de esa columna y se generará una ranura correspondiente en la salida con un estado de columna de JET_wrnColumnSkipped.

Si *ctagSequence* es 0 (cero) para un elemento determinado de la matriz de ID. de columna, se omite *rgtagSequence* y se enumeran todos los valores de columna para ese ID. de columna y se devuelven al autor de la llamada. Si un elemento de una matriz de números de *itagSequence* hace referencia a un número de *itagSequence* de 0 (cero), se omite la enumeración de ese número *itagSequence* y se generará una ranura correspondiente en la salida con un estado de valor de columna de JET_wrnColumnSkipped.

*rgEnumColumnId*

Vea *cEnumColumnId*.

*pcEnumColumn*

Devuelve la matriz enumerada de columnas y sus valores en la memoria asignada a través de la devolución de llamada compatible con *itagSequence* proporcionada.

Si se solicita una matriz de identificadores de columna en la entrada, el orden y el tamaño de la matriz de salida reflejarán el orden y el tamaño de la matriz de entrada. Del mismo modo, si se solicita una matriz de números *itagSequence* para un identificador de columna determinado en la entrada, el orden y el tamaño de la matriz de salida de los valores de columna de esa columna reflejará el orden y el tamaño de la matriz de entrada.

Los parámetros de salida se establecen en 0 (cero) y **null** en cualquier error, excepto en JET_errBadColumnId y JET_errColumnNotFound. Cuando se devuelven estos errores, los datos de salida son válidos y completos para todos los identificadores de columna afectados. El código de estado de cada uno de los identificadores de columna afectados se establece en uno de estos errores para que el autor de la llamada pueda determinar qué ID. de columna fueron incorrectos y, potencialmente, tomar medidas correctivas.

*prgEnumColumn*

Vea *pcEnumColumn*.

*pfnRealloc*

Identifica una devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) y un puntero de contexto opcional que se usa para asignar memoria para la matriz de salida de columnas y sus valores.

*pvReallocContext*

Vea *pfnRealloc*.

*cbDataMost*

Establece un límite en la cantidad de datos que se van a devolver de una columna de texto largo o binario largo.

Este parámetro se puede utilizar para evitar la enumeración de un valor de columna extremadamente grande. Normalmente, este tipo de enumeración podría producir un error en la llamada de API con JET_errOutOfMemory. Si un valor de columna grande se trunca de este modo, el estado del valor de la columna será JET_wrnColumnTruncated.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

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
<td><p>JET_bitEnumerateCompressOutput</p></td>
<td><p>Al enumerar los valores de columna, todas las columnas para las que se recuperan todos los valores y que solo tienen un valor de columna que no es NULL pueden devolverse en un formato comprimido. El estado de estas columnas se establecerá en JET_wrnColumnSingleValue y el tamaño del valor de columna y la memoria que contiene el valor de columna se devolverán directamente en la estructura de <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> . No se garantiza que todas las columnas coincidentes se compriman de esta manera. Consulte <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> para obtener más información.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateCopy</p></td>
<td><p>Esta opción indica que los valores de columna modificados del registro se deben enumerar en lugar de los valores de columna originales. Si un valor de columna no se ha modificado, se enumera el valor de la columna original. De esta manera, se puede enumerar un valor de columna que todavía no se ha insertado o actualizado al insertar o actualizar un registro.</p>
<p>Esta opción es idéntica a JET_bitRetrieveCopy cuando se usa con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateIgnoreDefault</p></td>
<td><p>Si una columna determinada no está presente en el registro, no se devolverá ningún valor de columna. Normalmente, el valor predeterminado de la columna, si existe, se devolvería en este caso. Se garantiza que, si la columna se establece en un valor distinto del valor predeterminado, se devolverá un valor diferente (es decir, si una columna con un valor predeterminado se establece explícitamente en <strong>null</strong> , se devolverá un valor <strong>null</strong> como valor para esa columna). Tenga en cuenta que, aunque se solicite esta opción, sigue siendo posible ver un valor de columna que sea igual al valor predeterminado. No se realiza ningún esfuerzo para quitar los valores de columna que coincidan con sus valores predeterminados.</p>
<p>Es importante tener en cuenta que esta opción afecta a la salida de <strong>JetEnumerateColumns</strong> cuando se usa con JET_bitEnumeratePresenceOnly o JET_bitEnumerateTaggedOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateIgnoreUserDefinedDefault</p></td>
<td><p>Si una columna determinada no está presente en el registro y tiene un valor predeterminado definido por el usuario, no se devolverá ningún valor de columna. Esta opción impedirá que se llame a la devolución de llamada que calcula el valor predeterminado definido por el usuario para la columna al enumerar los valores de esa columna.</p>
<p><strong>Windows Server 2003 y versiones anteriores:  </strong> En Windows Server 2003 y versiones anteriores, se producirá un error en la operación con JET_errCallbackFailed.</p>
<p><strong>Windows Server 2003 SP1:  </strong> Este valor posible solo está disponible para Windows Server 2003 SP1 y los sistemas operativos posteriores. Si se especifica este valor posible y la tabla contiene una columna que tiene un valor predeterminado definido por el usuario, se producirá un error en la operación con JET_errCallbackFailed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumeratePresenceOnly</p></td>
<td><p>Si existe un valor no NULL para el valor de columna o columna solicitado, no se devuelven los datos asociados. En su lugar, el estado asociado para ese valor de columna o columna se establecerá en JET_wrnColumnPresent. Si el valor de la columna o columna es <strong>null</strong> , JET_wrnColumnNull se devolverá como de costumbre.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateTaggedOnly</p></td>
<td><p>Al enumerar todos los valores de columna del registro (por ejemplo, es cuando <em>cEnumColumnId</em> es cero), solo se devolverán los valores de columna etiquetada. Esta opción no está permitida cuando se enumera una matriz de identificadores de columna específica.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateInRecordOnly</p></td>
<td><p><strong>Windows 7:  </strong> JET_bitEnumerateInRecordOnly se presenta en Windows 7.</p></td>
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
<td><p>El ID. de columna especificado está fuera de los límites legales de un identificador de columna. <strong>JetEnumerateColumns</strong> devolverá este error si se solicitaron ID. de columna específicos, uno de esos identificadores de columna no era válido y el primer ID. de columna no válido dio error en el código de estado de la columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La columna descrita por el ID. de columna especificado no existe en la tabla. <strong>JetEnumerateColumns</strong> devolverá este error si se solicitaron ID. de columna específicos, uno de esos identificadores de columna no era válido y el primer ID. de columna no válido dio error en el código de estado de la columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:  </strong> Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida o no se implementó. Este error lo devolverá <strong>JetEnumerateColumns</strong> cuando:</p>
<ul>
<li><p>Se especifica JET_bitEnumerateLocal.</p></li>
<li><p>Se ha especificado un <em>grbit</em> no válido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Este error lo devolverá <strong>JetEnumerateColumns</strong> cuando:</p>
<ul>
<li><p><em>pcEnumColumn</em> es <strong>null</strong>.</p></li>
<li><p><em>prgEnumColumn</em> es <strong>null</strong>.</p></li>
<li><p><em>pfnRealloc</em> es <strong>null</strong>.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está situado en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>El cursor se coloca en un registro que se ha eliminado. Esto puede ocurrir por diversos motivos. La razón más común es que la sesión no está en una transacción, el cursor se colocó en un registro, se eliminó el registro y, a continuación, el cursor intentó hacer referencia a ese registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:  </strong> Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, los datos solicitados se devolverán en los búferes de salida. Es responsabilidad del llamador liberar cualquier memoria asignada por esta devolución de llamada y devolverla en los búferes de salida. Esa memoria se debe liberar mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) proporcionada. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, no se devolverá ninguno de los datos solicitados. Cualquier memoria asignada durante la llamada se liberará automáticamente mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) proporcionada. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Si está enumerando todos los valores de columna del registro y no especificó JET_bitEnumerateIgnoreDefaults, no puede suponer que nunca verá un valor de columna o columna con un código de estado de JET_wrnColumnNull. Puede ver este código de estado si una columna tiene un valor predeterminado y se estableció explícitamente en **null** o si la columna es una columna no dispersa (por ejemplo, una columna fija o variable).

El parámetro *cbDataMost* no se aplica a todos los valores de columna. Este parámetro solo truncará los valores de texto largo y de columna binaria larga que son tan grandes que se han almacenado por separado del registro.

Si **JetEnumerateColumns** devuelve datos en sus parámetros de salida, el llamador es responsable de liberar la memoria de la matriz, así como cualquier memoria a la que hacen referencia los punteros incrustados en esa matriz.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JET_PFNREALLOC](./jet-pfnrealloc-callback-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
