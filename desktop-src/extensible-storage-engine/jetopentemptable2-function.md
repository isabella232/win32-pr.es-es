---
description: 'Más información sobre: JetOpenTempTable2 (Función)'
title: Función JetOpenTempTable2
TOCTitle: JetOpenTempTable2 Function
ms:assetid: 788ec4f9-b0c3-409b-850c-7567dec47024
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269302(v=EXCHG.10)
ms:contentKeyID: 32765594
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f6ac33866ea2f58c6dc5de593aeed046c981c48c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984478"
---
# <a name="jetopentemptable2-function"></a>Función JetOpenTempTable2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetopentemptable2-function"></a>Función JetOpenTempTable2

La **función JetOpenTempTable2** crea una tabla temporal con un único índice que se puede usar para almacenar y recuperar registros igual que una tabla normal creada con [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Esta función también tiene un identificador de configuración regional que se puede usar para comparar datos de columna de clave Unicode en la tabla temporal. Sin embargo, las tablas temporales son mucho más rápidas que las tablas normales debido a su naturaleza volátil. También se pueden usar para ordenar y realizar la eliminación de duplicados rápidamente en conjuntos de registros cuando se accede a ellos de una manera puramente secuencial.

```cpp
    JET_ERR JET_API JetOpenTempTable2(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          unsigned long lcid,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se usará.

*prgcolumndef*

Definiciones de columna de las columnas que se crearán en la tabla temporal.

Existen limitaciones importantes para las opciones de definición de columna que se usan con una tabla temporal. Vea la sección Comentarios para obtener más información.

Además de las opciones habituales de definición de columna, también se pueden especificar cero o más de las siguientes opciones que solo son pertinentes en el contexto de una tabla temporal.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>El criterio de ordenación de la columna de clave de la tabla temporal debe ser descendente en lugar de ascendente. Si esta opción se especifica sin JET_bitColumnTTKey, esta opción se omite.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>La columna será una columna de clave para la tabla temporal.</p><p>El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal. La primera definición de columna de la matriz con este conjunto de opciones será la columna de clave más significativa, y así sucesivamente. Si se solicitan más columnas de clave de las que puede ser compatible con el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</p> | 



*ccolumn*

Vea *prgcolumndef*.

*lcid*

Identificador de configuración regional que se usará para comparar los datos de columna de clave Unicode de la tabla temporal.

Se puede usar cualquier configuración regional siempre que se haya instalado el paquete de idioma adecuado en la máquina. La única excepción es que la configuración regional de idioma neutro (LCID de cero) no es posible.

En Windows Server 2003 y versiones posteriores, si se especifica la configuración regional de idioma neutro para este parámetro, se usará en su lugar el identificador de configuración regional predeterminado (inglés de EE. UU.). Esto permite que un valor de cero signifique el valor predeterminado en lugar de un valor no válido.

Cuando este parámetro no está presente y el *parámetro pidxunicode* no está presente, se usará el LCID predeterminado para comparar los datos de columna de clave Unicode de la tabla temporal. El LCID predeterminado es la configuración regional del inglés de EE. UU.

*grbit*

Grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Esta opción solicita que cualquier intento de insertar un registro con la misma clave de índice que un registro insertado anteriormente producirá un error inmediatamente con JET_errKeyDuplicate. Si no se solicita esta opción, se puede detectar inmediatamente un duplicado y producir un error o se puede quitar de forma silenciosa más adelante, en función de la estrategia elegida por el motor de base de datos para implementar la tabla temporal en función de la funcionalidad solicitada.</p><p>Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Esta opción obliga al administrador de tablas temporales a abandonar cualquier intento de elegir una estrategia inteligente para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>Esta opción solicita que la tabla temporal solo se cree si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta. Si alguna característica de la tabla temporal impediría el uso de esta optimización, se producirá un error en la operación JET_errCannotMaterializeForwardOnlySort.</p><p>Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas. Consulte JET_bitTTUnique para obtener más información.</p><p>Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</p> | 
| <p>JET_bitTTIndexed</p> | <p>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para buscar registros por clave de índice.</p><p>Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se digitalizarán en orden y dirección arbitrarios <a href="gg294117(v=exchg.10).md">mediante JetMove</a>.</p><p>Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Esta opción solicita que los valores de columna de clave NULL se ordenan más cerca del final del índice que los valores de columna de clave no NULL.</p> | 
| <p>JET_bitTTUnique</p> | <p>Esta opción solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</p><p>Antes de Windows Server 2003, el motor de base de datos siempre presumía que esta opción estaba en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos. A partir Windows Server 2003, ahora es posible crear una tabla temporal que NO quite duplicados cuando también se especifique la opción JET_bitTTForwardOnly servidor.</p><p>No es posible saber qué duplicado ganará y qué duplicados se descartarán en general. Sin embargo, cuando se JET_bitTTErrorOnDuplicateInsertion la opción , siempre ganará el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros que se han insertado anteriormente se cambien posteriormente. Si esta funcionalidad no es necesaria, es mejor no solicitarla.</p><p>Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>Solicitudes para permitir solo valores long intrínsecos.</p><p><strong>Windows 7:</strong> <strong>JET_bitTTIntrinsicLVsOnly</strong> se introdujo en Windows 7.</p> | 



*ptableid*

Búfer de salida que recibirá el nuevo cursor abierto en la tabla temporal recién creada.

*prgcolumnid*

Búfer de salida que recibirá la matriz de id. de columna generados durante la creación de la tabla temporal.

Los id. de columna de esta matriz se corresponderán exactamente con la matriz de entrada de definiciones de columna. Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>Error de JetOpenTempTable2</strong> porque JET_bitTTForwardOnly se especificó y la tabla temporal especificada no se pudo crear mediante la optimización de solo avance. Este error solo lo devolverá Windows Server 2003 y versiones posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>El campo cp del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se estableció en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (inglés, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>El <em>campo coltyp</em> del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se estableció en un tipo de columna válido.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>No se pudo crear el índice porque se especificó una definición de índice no válida.</p><p><strong>JetOpenTempTable2</strong> devolverá este error cuando:</p><ul><li><p>Se especifica la configuración regional idioma neutro.</p></li><li><p>Se especifica un conjunto no válido de marcas de normalización.</p></li></ul><p>Este error solo lo devolverá Windows 2000.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>No se pudo crear el índice porque se intentó usar un identificador de configuración regional no válido. El identificador de configuración regional puede ser completamente no válido o es posible que el paquete de idioma asociado no esté instalado.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>No se pudo crear el índice porque se intentó usar un conjunto no válido de marcas de normalización. Este error solo lo devolverán Windows XP y versiones posteriores. En Windows 2000, las marcas de normalización no válidas darán lugar a JET_errIndexInvalidDef en su lugar.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Error en la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor. Los recursos de cursor se configuran <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxCursors</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar suficiente memoria para completarla.</p><p><strong>JetOpenTempTable2 puede</strong> devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host se vuelve demasiado fragmentado. El administrador de tablas temporales siempre asignará un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, no más de JET_ccolVarMost columnas de longitud variable y no más de JET_ccolTaggedMost columnas etiquetadas.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>Error en la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché los índices de la tabla. El número de índices cuyo esquema se puede almacenar en caché se configura <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Error en la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché el esquema de la tabla. El número de tablas cuyo esquema se puede almacenar en caché se configura <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errTooManySorts</p> | <p>Error en la operación porque el motor no puede asignar los recursos necesarios para crear una tabla temporal. Los recursos de tabla temporales se configuran <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg294140(v=exchg.10).md">con JET_paramMaxTemporaryTables</a>.</p> | 



Si se ejecuta correctamente, se devolverá un cursor abierto en la tabla temporal recién creada. El estado de la base de datos temporal se preparará para contener la nueva tabla temporal. El estado de las bases de datos normales en uso por el motor de base de datos permanecerá sin cambios.

En caso de error, no se creará la tabla temporal y no se devolverá un cursor. Se puede cambiar el estado de la base de datos temporal. El estado de las bases de datos normales en uso por el motor de base de datos permanecerá sin cambios.

#### <a name="remarks"></a>Observaciones

Consulte [JetOpenTempTable](./jetopentemptable-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
