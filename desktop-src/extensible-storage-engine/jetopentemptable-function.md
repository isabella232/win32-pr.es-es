---
description: 'Más información sobre: JetOpenTempTable (Función)'
title: Función JetOpenTempTable
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f2aa3fdd1ae95fa377f65b5422a2a236868fc62
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469772"
---
# <a name="jetopentemptable-function"></a>Función JetOpenTempTable


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetopentemptable-function"></a>Función JetOpenTempTable

La **función JetOpenTempTable** crea una tabla temporal con un único índice. Una tabla temporal almacena y recupera registros igual que una tabla normal creada [mediante JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Sin embargo, las tablas temporales son mucho más rápidas que las tablas normales debido a su naturaleza volátil. También se pueden usar para ordenar y realizar la eliminación de duplicados rápidamente en conjuntos de registros cuando se accede a ellos de una manera puramente secuencial.

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se usará.

*prgcolumndef*

Definiciones de columna para las columnas creadas en la tabla temporal.

**Existen**   limitaciones importantes para las opciones de definición de columna que se usan con una tabla temporal. Vea la sección Comentarios para obtener más información.

Además de las opciones de definición de columna habituales, también se pueden especificar cero o más de las siguientes opciones que solo son pertinentes en el contexto de una tabla temporal.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>El criterio de ordenación de la columna de clave de la tabla temporal debe ser descendente en lugar de ascendente. Si esta opción se especifica sin JET_bitColumnTTKey, se omite esta opción.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>La columna será una columna de clave para la tabla temporal.</p><p>El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal. La primera definición de columna de la matriz que tiene esta opción establecida será la columna de clave más importante, y así sucesivamente. Si se solicitan más columnas de clave de las que puede ser compatibles con el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</p> | 



*ccolumn*

Vea *prgcolumndef*.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Cualquier intento de insertar un registro con la misma clave de índice que un registro insertado previamente producirá un error JET_errKeyDuplicate. Si no se solicita esta opción, se detecta inmediatamente un duplicado y se produce un error, o se quita de forma silenciosa más adelante, en función de la estrategia elegida por el motor de base de datos para implementar la tabla temporal, en función de la funcionalidad solicitada.</p><p>Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Obliga al administrador de tablas temporales a abandonar la búsqueda de la mejor estrategia para usar la administración de la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>La tabla temporal solo se crea si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta. Si alguna característica de la tabla temporal impediría el uso de esta optimización, se producirá un error en la operación JET_errCannotMaterializeForwardOnlySort.</p><p>Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas. Consulte JET_bitTTUnique para obtener más información.</p><p>Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</p> | 
| <p>JET_bitTTIndexed</p> | <p>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para buscar registros por clave de índice.</p><p>Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p> | 
| <p>JET_bitTTUnique</p> | <p>Solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</p><p>Antes de Windows Server 2003, el motor de base de datos siempre supusía que esta opción estaba en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos. A partir Windows Server 2003, ahora es posible crear una tabla temporal que no quite duplicados cuando también se especifique la opción JET_bitTTForwardOnly .</p><p>No es posible saber qué duplicado se realizará correctamente y qué duplicados se descartarán, en general. Sin embargo, cuando JET_bitTTErrorOnDuplicateInsertion se solicita la opción , el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre se realizará correctamente.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros que se han insertado previamente se cambien posteriormente. Si esta funcionalidad no es necesaria, es mejor no solicitarla.</p><p>Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se digitalizarán en orden y dirección arbitrarios <a href="gg294117(v=exchg.10).md">mediante JetMove</a>.</p><p>Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Solicita que los valores de columna de clave NULL se ordenan más cerca del final del índice que los valores de columna de clave no NULL.</p><p></p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>Solicita que solo se permitan valores long intrínsecos.</p><p><strong>Windows 7:</strong> <strong>JET_bitTTIntrinsicLVsOnly</strong> se introdujo en Windows 7.</p> | 



*ptableid*

Búfer de salida que recibe el nuevo cursor abierto en la tabla temporal recién creada.

*prgcolumnid*

Búfer de salida que recibe la matriz de id. de columna generados durante la creación de la tabla temporal.

Los id. de columna de esta matriz se corresponderán exactamente con la matriz de entrada de definiciones de columna. Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>Error de JetOpenTempTable</strong> porque JET_bitTTForwardOnly se especificó y no se pudo crear la tabla temporal especificada mediante la optimización de solo avance. Este error solo lo devolverán Windows Server 2003 y versiones posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>No se pudo crear el índice porque se especificó una definición de índice no válida.</p><p><strong>JetOpenTempTable</strong> devolverá este error cuando:</p><ul><li><p>Se especifica la configuración regional idioma neutro.</p></li><li><p>Se especifica un conjunto de marcas de normalización no válido.</p></li></ul><p>Este error solo lo devolverá Windows 2000.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>El campo cp del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se estableció en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (inglés, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>El <em>campo coltyp</em> del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se estableció en un tipo de columna válido.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>No se pudo crear el índice porque se intentó usar un identificador de configuración regional no válido. El identificador de configuración regional puede ser completamente no válido o es posible que el paquete de idioma asociado no esté instalado.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>No se pudo crear el índice porque se intentó usar un conjunto no válido de marcas de normalización. Este error solo lo devolverán Windows XP y versiones posteriores. En Windows 2000, las marcas de normalización no válidas darán lugar a JET_errIndexInvalidDef en su lugar.</p> | 
| <p>JET_errInvalidSesid</p> | <p>El identificador de sesión no es válido o hace referencia a una sesión cerrada.</p><p><strong>Nota</strong>  Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Error en la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor. Los recursos de cursor se configuran <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxCursors</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar suficiente memoria para completarla.</p><p><strong>JetOpenTempTable puede</strong> devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host se fragmenta demasiado. El administrador de tablas temporales siempre asignará un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, no más de JET_ccolVarMost columnas de longitud variable y no más de JET_ccolTaggedMost columnas etiquetadas.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>Error en la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché los índices de la tabla. El número de índices cuyo esquema se puede almacenar en caché se configura <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Error en la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché el esquema de la tabla. El número de tablas cuyo esquema se puede almacenar en caché se configura <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errTooManySorts</p> | <p>Error en la operación porque el motor no puede asignar los recursos necesarios para crear una tabla temporal. Los recursos de tabla temporales se configuran <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg294140(v=exchg.10).md">con JET_paramMaxTemporaryTables</a>.</p> | 



Si se ejecuta correctamente, se devolverá un cursor abierto en la tabla temporal recién creada. El estado de la base de datos temporal se preparará para contener la nueva tabla temporal. El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.

En caso de error, no se creará la tabla temporal y no se devolverá un cursor. Se puede cambiar el estado de la base de datos temporal. El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.

#### <a name="remarks"></a>Comentarios

Las tablas temporales no admiten el complemento completo de las opciones de definición de columna que normalmente admite el motor de base de datos. De hecho, solo JET_bitColumnFixed y JET_bitColumnTagged se admiten. Esto significa que no es posible crear una columna de incremento automático, versión o multivalor en una tabla temporal. Por último, las columnas de actualización de custodia no se admiten porque no son útiles en una tabla temporal, ya que solo las puede usar una sesión a la vez. Si se solicita cualquiera de estas opciones, se omitirán.

Las tablas temporales no admiten valores predeterminados. Si se proporciona una definición de columna que contiene una especificación de valor predeterminada, esa especificación se omitirá.

Las tablas temporales se devuelven al autor de la llamada como resultado de muchas funciones ese diferentes. Por ejemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md) con la opción JET_IdxInfo establecida en el parámetro *InfoLevel* devolverá una tabla temporal que contiene una lista de todas las columnas de clave de un índice determinado. Las tablas temporales siguen las mismas reglas de ciclo de vida que las tablas temporales normales, como se describe aquí.

El motor de base de datos también usa internamente tablas temporales para muchas tareas. La más importante de estas tareas es la creación de un índice sobre una tabla existente. Se usará una tabla temporal para ordenar las claves de índice usadas para construir ese índice.

Todas las tablas temporales se almacenan en la base de datos temporal. La base de datos temporal es un archivo de base de datos especial que se mantiene durante la vigencia de una instancia de ESE y se elimina cuando esa instancia se cierra o reinicia. La ubicación de la base de datos temporal se puede configurar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) [con JET_paramTempPath](./temporary-database-parameters.md). La ubicación de la base de datos temporal en el disco en relación con los archivos de registro de transacciones y los archivos de base de datos puede ser importante si la aplicación hace un uso pesado de las tablas temporales o crea índices con frecuencia.

El ciclo de vida de una tabla temporal está asociado a los cursores que hacen referencia a ella. Si se cierran todos los cursores que hacen referencia a una tabla temporal, ya sea implícita o explícitamente, se eliminará la tabla temporal. Si se crea una tabla temporal dentro de una transacción y esa transacción se revierte posteriormente, se eliminará la tabla temporal porque los cursores que hacen referencia a ella en este momento se cerrarán implícitamente. Los nuevos cursores pueden hacer referencia a una tabla temporal solo mediante el uso de [JetDupCursor](./jetdupcursor-function.md). En este caso, los nuevos cursores se colocarán en la primera entrada de índice de la tabla temporal. [JetDupCursor](./jetdupcursor-function.md) solo funcionará durante determinadas fases de uso para la tabla temporal. Consulte los comentarios relativos a las funcionalidades de cursor de tabla temporal para obtener más información. No es posible hacer referencia a una tabla temporal de más de una sesión a la vez.

Hay un problema importante en [JetDupCursor](./jetdupcursor-function.md) que afecta a las tablas temporales. Si se intenta duplicar una tabla temporal que está en modo de solo avance, el cursor resultante no se creará correctamente y no se realizará correctamente. Todavía es seguro duplicar un cursor sobre una tabla temporal materializada.

El administrador de tablas temporales puede optar por implementar una tabla temporal de tres maneras. El primer método consiste en mantener una tabla en memoria. Esta estrategia es la más rápida, pero solo se puede usar para tablas temporales pequeñas y sencillas. El segundo método consiste en crear una ordenación basada en disco que se pueda basar mediante un iterador de solo avance. Esta estrategia solo se puede usar en determinadas circunstancias y es la manera más rápida de ordenar y quitar duplicados de un conjunto de datos muy grande. El tercer método consiste en crear un árbol B+ en la base de datos temporal para contener la tabla temporal. Esta estrategia es la más lenta, pero la más versátil, y se conoce como tabla temporal materializada. Estas estrategias se pueden usar en combinación para lograr en última instancia la funcionalidad solicitada de la tabla temporal.

Cuando la tabla temporal no se materializa, se usa principalmente en dos fases principales. La primera fase es la fase de inserción donde la tabla se rellena con su conjunto de datos inicial. Durante esta fase, solo se permite la inserción de datos. Esta fase finaliza cuando se intenta mover el cursor mediante [JetMove](./jetmove-function.md) o [JetSeek](./jetseek-function.md). La segunda fase es la fase de extracción de datos. Durante esta fase, los datos almacenados en la tabla temporal se pueden extraer según las funcionalidades solicitadas cuando se creó la tabla temporal.

**Funcionalidades de cursor de tabla temporal**

Cuando se materializa la tabla temporal, el cursor tiene las siguientes funcionalidades, pero puede estar aún más limitado por las opciones solicitadas:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDelete](./jetdelete-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUpdate](./jetupdate-function.md)

Cuando la tabla temporal no se materializa y se encuentra en la fase de inserción, el cursor tiene las siguientes funcionalidades, pero puede estar aún más limitado por las opciones solicitadas:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)
    
    **Nota**  Provoca la transición a la fase de extracción.

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)
    
    **Nota**  Provoca la transición a la fase de extracción.

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetUpdate](./jetupdate-function.md)

Cuando la tabla temporal no se materializa y se encuentra en la fase de extracción, el cursor tiene las siguientes funcionalidades, pero puede estar aún más limitado por las opciones solicitadas:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)
    
    **Nota**  Si se intenta duplicar una tabla temporal que está en modo de solo avance, el cursor resultante no se creará correctamente y no se realizará correctamente. Todavía es seguro duplicar un cursor sobre una tabla temporal materializada.

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



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
[Parámetros temporales de base de datos](./temporary-database-parameters.md)
