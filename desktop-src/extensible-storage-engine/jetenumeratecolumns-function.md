---
description: 'Más información sobre: JetEnumerateColumns (Función)'
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
ms.openlocfilehash: 9a9d5b8d32db7fdb786edc7aaade92bf2e074080
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988087"
---
# <a name="jetenumeratecolumns-function"></a>Función JetEnumerateColumns


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetenumeratecolumns-function"></a>Función JetEnumerateColumns

La **función JetEnumerateColumns** recupera eficazmente un conjunto de columnas y sus valores del registro actual de un cursor o del búfer de copia de ese cursor. Las columnas y los valores recuperados se pueden restringir mediante una lista de id. de columna, números *de itagSequence* y otras características. Esta API de recuperación de columnas es única en que devuelve información en memoria asignada dinámicamente que se obtiene mediante una devolución de llamada compatible con [el reasignación](/cpp/c-runtime-library/reference/realloc?view=vs-2019) proporcionada por el usuario. Esta nueva flexibilidad permite la recuperación eficaz de datos de columna con características específicas (como el tamaño y la multiplicidad) que el autor de la llamada desconoce. Esto elimina la necesidad de usar los modos de detección de [JetRetrieveColumn](./jetretrievecolumn-function.md) para determinar esas características con el fin de configurar una llamada final a [JetRetrieveColumn](./jetretrievecolumn-function.md) que recupere correctamente los datos deseados.

**Windows XP: JetEnumerateColumns** se introdujo en Windows XP.

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

*tableid*

Cursor que se va a usar para esta llamada.

*cEnumColumnId*

Matriz de id. de columna, cada uno con una matriz opcional de números *de itagSequence* que se va a enumerar.

Si *cEnumColumnId* es 0 (cero), se omite *rgEnumColumnId* y todos los valores de columna se enumeran y se devuelven al autor de la llamada. Si un elemento de la matriz de identificadores de columna hace referencia a un identificador de columna de 0 (cero), se omite la enumeración de esa columna y se genera una ranura correspondiente en la salida con un estado de columna de JET_wrnColumnSkipped.

Si *ctagSequence* es 0 (cero) para un elemento determinado de la matriz de identificadores de columna, se omite *rgtagSequence* y todos los valores de columna de ese identificador de columna se enumeran y se devuelven al autor de la llamada. Si un elemento de una matriz de números *de itagSequence* hace referencia a un número de *itagSequence* de 0 (cero), se omite la enumeración de ese número *de itagSequence* y se generará una ranura correspondiente en la salida con un estado de valor de columna de JET_wrnColumnSkipped.

*rgEnumColumnId*

Vea *cEnumColumnId*.

*pcEnumColumn*

Devuelve la matriz enumerada de columnas y sus valores en memoria asignados a través de la devolución de llamada compatible *con itagSequence* proporcionada.

Si se solicita una matriz de id. de columna en la entrada, el orden y el tamaño de la matriz de salida reflejarán el orden y el tamaño de la matriz de entrada. Del mismo modo, si se solicita una matriz de números *itagSequence* para un identificador de columna determinado en la entrada, el orden y el tamaño de la matriz de salida de valores de columna para esa columna reflejarán el orden y el tamaño de la matriz de entrada.

Los parámetros de salida se establecen en 0 (cero) y **NULL** en cualquier error, excepto JET_errBadColumnId y JET_errColumnNotFound. Cuando se devuelven estos errores, los datos de salida son válidos y completos para todos los identificadores de columna, menos los identificadores de columna afectados. El código de estado de cada uno de los identificadores de columna afectados se establece en uno de estos errores para que el autor de la llamada pueda determinar qué identificadores de columna eran correctos y, potencialmente, tomar medidas correctivas.

*prgEnumColumn*

Vea *pcEnumColumn*.

*pfnRealloc*

Identifica una devolución de llamada compatible con [reasignación](/cpp/c-runtime-library/reference/realloc?view=vs-2019) y un puntero de contexto opcional que se usa para asignar memoria para la matriz de salida de columnas y sus valores.

*pvReallocContext*

Vea *pfnRealloc*.

*cbDataMost*

Establece un límite en la cantidad de datos que se devolverán de una columna de texto largo o binario largo.

Este parámetro se puede usar para evitar la enumeración de un valor de columna extremadamente grande. Normalmente, este tipo de enumeración podría producir un error en la llamada API con JET_errOutOfMemory. Si un valor de columna grande se trunca de tal manera, el estado del valor de columna se JET_wrnColumnTruncated.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitEnumerateCompressOutput</p> | <p>Al enumerar valores de columna, todas las columnas para las que se recuperan todos los valores y que tienen solo un valor de columna distinto de NULL se pueden devolver en un formato comprimido. El estado de estas columnas se establecerá en JET_wrnColumnSingleValue y el tamaño del valor de columna y la memoria que contiene el valor de columna se devolverán directamente en la <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> columna. No se garantiza que todas las columnas aptas se comprimen de esta manera. Consulte <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> para obtener más información.</p> | 
| <p>JET_bitEnumerateCopy</p> | <p>Esta opción indica que los valores de columna modificados del registro deben enumerarse en lugar de los valores de columna originales. Si no se ha modificado un valor de columna, se enumera el valor de columna original. De este modo, se puede enumerar un valor de columna que aún no se ha insertado o actualizado al insertar o actualizar un registro.</p><p>Esta opción es idéntica a JET_bitRetrieveCopy cuando se usa <a href="gg269198(v=exchg.10).md">con JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns.</a></p> | 
| <p>JET_bitEnumerateIgnoreDefault</p> | <p>Si una columna determinada no está presente en el registro, no se devolverá ningún valor de columna. Normalmente, el valor predeterminado de la columna, si lo hubiera, se devolvería en este caso. Se garantiza que si la columna se establece en un valor diferente del valor predeterminado, se devolverá ese valor diferente (es decir, si una columna con un valor predeterminado se establece explícitamente en <strong>NULL,</strong> se devolverá un valor <strong>NULL</strong> como valor de esa columna). Tenga en cuenta que, incluso si se solicita esta opción, todavía es posible ver un valor de columna que sea igual al valor predeterminado. No se realiza ningún esfuerzo para quitar valores de columna que coincidan con sus valores predeterminados.</p><p>Es importante tener en cuenta que esta opción afecta a la salida de <strong>JetEnumerateColumns</strong> cuando se usa con JET_bitEnumeratePresenceOnly o JET_bitEnumerateTaggedOnly.</p> | 
| <p>JET_bitEnumerateIgnoreUserDefinedDefault</p> | <p>Si una columna determinada no está presente en el registro y tiene un valor predeterminado definido por el usuario, no se devolverá ningún valor de columna. Esta opción impedirá que se llame a la devolución de llamada que calcula el valor predeterminado definido por el usuario para la columna al enumerar los valores de esa columna.</p><p><strong>Windows Server 2003 y versiones anteriores:</strong> Para Windows Server 2003 y versiones anteriores, se producirá un error en la operación JET_errCallbackFailed.</p><p><strong>Windows Server 2003 SP1:</strong> Este valor posible solo está disponible para Windows Server 2003 SP1 y sistemas operativos posteriores. Si se especifica este valor posible y la tabla contiene una columna que tiene un valor predeterminado definido por el usuario, se producirá un error en la operación JET_errCallbackFailed.</p> | 
| <p>JET_bitEnumeratePresenceOnly</p> | <p>Si existe un valor distinto de NULL para el valor de columna o columna solicitado, no se devuelven los datos asociados. En su lugar, el estado asociado para ese valor de columna o columna se establecerá en JET_wrnColumnPresent. Si el valor de columna o columna es <strong>NULL,</strong> JET_wrnColumnNull se devolverá como de costumbre.</p> | 
| <p>JET_bitEnumerateTaggedOnly</p> | <p>Al enumerar todos los valores de columna en el registro (por ejemplo, cuando <em>cEnumColumnId</em> es cero), solo se devolverán los valores de columna etiquetados. Esta opción no se permite al enumerar una matriz específica de id. de columna.</p> | 
| <p>JET_bitEnumerateInRecordOnly</p> | <p><strong>Windows 7:</strong> JET_bitEnumerateInRecordOnly se introdujo en Windows 7.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBadColumnId</p> | <p>El identificador de columna especificado está fuera de los límites legales de un identificador de columna. <strong>JetEnumerateColumns</strong> devolverá este error si se solicitaron identificadores de columna específicos, uno de esos identificadores de columna no era válido y el primer identificador de columna no válido produjo este error para su código de estado de columna.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La columna descrita por el identificador de columna especificado no existe en la tabla. <strong>JetEnumerateColumns</strong> devolverá este error si se solicitaron identificadores de columna específicos, uno de esos identificadores de columna no era válido y el primer identificador de columna no válido produjo este error para su código de estado de columna.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong> Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una de las opciones solicitadas no era válida o no se implementó. <strong>JetEnumerateColumns</strong> devolverá este error cuando:</p><ul><li><p>JET_bitEnumerateLocal se especifica .</p></li><li><p>Se especifica <em>un grbit</em> no es así.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. <strong>JetEnumerateColumns</strong> devolverá este error cuando:</p><ul><li><p><em>pcEnumColumn</em> es <strong>NULL.</strong></p></li><li><p><em>prgEnumColumn</em> es <strong>NULL.</strong></p></li><li><p><em>pfnRealloc</em> es <strong>NULL.</strong></p></li></ul> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no está situado en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor se coloca actualmente después del último registro en el índice actual.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRecordDeleted</p> | <p>El cursor se coloca en un registro que se ha eliminado. Esto puede ocurrir por diversos motivos. La razón más común es que la sesión no está en una transacción, el cursor se ha situado en un registro, ese registro se ha eliminado y, a continuación, el cursor ha intentado hacer referencia a ese registro.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong> Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, los datos solicitados se devolverán en los búferes de salida. Es responsabilidad del autor de la llamada liberar cualquier memoria asignada por esta devolución de llamada y devuelta en los búferes de salida. Esa memoria se debe liberar a través de la devolución de llamada [compatible con el](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación proporcionada. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, no se devolverá ninguno de los datos solicitados. Cualquier memoria que se asignó durante la llamada se liberará automáticamente mediante la devolución de llamada [compatible con la](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación proporcionada. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Si enumera todos los valores de columna en el registro y no ha especificado JET_bitEnumerateIgnoreDefaults no puede suponer que nunca verá un valor de columna o columna con un código de estado de JET_wrnColumnNull. Puede ver este código de estado si una columna tiene un valor predeterminado y se estableció explícitamente en **NULL** o si la columna es una columna no dispersa (por ejemplo, una columna fija o variable).

El *parámetro cbDataMost* no se aplica a todos los valores de columna. Este parámetro solo truncará los valores de texto largo y de columna binaria larga que son tan grandes que se han almacenado por separado del registro.

Si **JetEnumerateColumns** devuelve datos en sus parámetros de salida, el autor de la llamada es responsable de liberar la memoria de la matriz, así como de la memoria a la que se hace referencia mediante punteros incrustados en esa matriz.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



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
