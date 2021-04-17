---
description: 'Más información acerca de: JetOpenTempTable3 (función)'
title: Función JetOpenTempTable3
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7820f90ef0192c1f700759835bf1572b187cf3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696216"
---
# <a name="jetopentemptable3-function"></a>Función JetOpenTempTable3


_**Se aplica a:** Windows | Windows Server_

## <a name="jetopentemptable3-function"></a>Función JetOpenTempTable3

La función **JetOpenTempTable3** crea una tabla temporal con un índice único que se puede usar para almacenar y recuperar registros como una tabla normal creada con [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil. También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*prgcolumndef*

Identifica las definiciones de columna de las columnas que se van a crear en la tabla temporal.

Existen limitaciones importantes en las opciones de definición de columna que se pueden usar con una tabla temporal. Vea la sección Comentarios para obtener más información.

Además de las opciones de definición de columna habituales, también se pueden especificar cero o más de las opciones siguientes que solo son relevantes en el contexto de una tabla temporal.

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
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Esta opción indica que el criterio de ordenación de la columna de clave para la tabla temporal debe ser descendente en lugar de ascendente. Si se especifica esta opción sin JET_bitColumnTTKey, se omite esta opción.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Esta opción indica que la columna será una columna de clave para la tabla temporal.</p>
<p>El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal. La primera definición de columna de la matriz con esta opción establecida será la columna de clave más significativa, etc. Si se solicitan más columnas de clave de las que puede admitir el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</p></td>
</tr>
</tbody>
</table>


*ccolumn*

Vea *prgcolumndef*.

*pidxunicode*

El identificador de configuración regional y las marcas de normalización que se utilizarán para comparar los datos de columna de clave Unicode en la tabla temporal.

Cuando este parámetro no está presente, se usará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal. El LCID predeterminado es la configuración regional en Inglés de EE. UU.

Cuando este parámetro no está presente, se usarán las marcas de normalización predeterminadas para comparar los datos de columna de clave Unicode en la tabla temporal. Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.

*grbit*

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.

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
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Esta opción solicita que se produzca inmediatamente un error al intentar insertar un registro con la misma clave de índice que un registro insertado previamente con JET_errKeyDuplicate. Si no se solicita esta opción, un duplicado puede detectarse inmediatamente y producir un error, o bien se puede quitar de forma silenciosa más adelante según la estrategia elegida por el motor de base de datos para implementar la tabla temporal en función de la funcionalidad solicitada.</p>
<p>Si esta funcionalidad no es necesaria, es mejor no solicitarlo. Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Esta opción obliga al administrador de tablas temporales a abandonar cualquier intento de elegir una estrategia de Clever para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>Esta opción solicita que la tabla temporal se cree solo si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta. Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort.</p>
<p>Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas. Consulte JET_bitTTUnique para obtener más información.</p>
<p>Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTIndexed</p></td>
<td><p>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para buscar registros por clave de índice.</p>
<p>Si esta funcionalidad no es necesaria, es mejor no solicitarlo. Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUnique</p></td>
<td><p>Esta opción solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</p>
<p>Antes de Windows Server 2003, el motor de base de datos siempre asumió que esta opción está en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos. A partir de Windows Server 2003, ahora es posible crear una tabla temporal que no quita los duplicados cuando también se especifica la opción de JET_bitTTForwardOnly.</p>
<p>No es posible saber qué duplicado ganará y qué duplicados se descartarán en general. Sin embargo, cuando se solicita la opción de JET_bitTTErrorOnDuplicateInsertion, el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre ganará.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que se modifiquen posteriormente los registros que se han insertado previamente. Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</p>
<p>Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se examinen en orden y dirección arbitrarios con <a href="gg294117(v=exchg.10).md">JetMove</a>.</p>
<p>Si esta funcionalidad no es necesaria, es mejor no solicitarlo. Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Esta opción solicita que los valores de columna de clave NULL se ordenen más cerca del final del índice que los valores de columna de clave no NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTIntrinsicLVsOnly</p></td>
<td><p>Solicitudes para permitir solo valores largos intrínsecos.</p>
<p><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> se introduce en Windows 7.</p></td>
</tr>
</tbody>
</table>


*ptableid*

Búfer de salida que recibirá el nuevo cursor abierto en la tabla temporal recién creada.

*prgcolumnid*

Búfer de salida que recibirá la matriz de identificadores de columna generados durante la creación de la tabla temporal.

Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna. Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.

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
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p>Error de <strong>JetOpenTempTable3</strong> porque se especificó JET_bitTTForwardOnly y no se pudo crear la tabla temporal tal y como se especificó mediante la optimización de solo avance. Este error solo lo devolverán Windows Server 2003 y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>No se pudo crear el índice porque se especificó una definición de índice no válida. <strong>JetOpenTempTable3</strong> devolverá este error cuando:</p>
<ul>
<li><p>Se especifica la configuración regional independiente del idioma.</p></li>
<li><p>Se especifica un conjunto no válido de marcas de normalización.</p></li>
</ul>
<p>Este error solo lo devolverá Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>El miembro <strong>CP</strong> de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>El miembro <strong>coltyp</strong> de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en un tipo de columna válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>No se pudo crear el índice porque se intentó usar un ID. de configuración regional no válido. Es posible que el ID. de configuración regional no sea válido o que el paquete de idioma asociado no esté instalado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>No se pudo crear el índice porque se intentó usar un conjunto no válido de marcas de normalización. Este error solo se devolverá en Windows XP y versiones posteriores. En Windows 2000, las marcas de normalización no válidas producirán JET_errIndexInvalidDef en su lugar.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>El identificador de sesión no es válido o hace referencia a una sesión cerrada. Este error no se devuelve en todas las circunstancias. Los identificadores se validan solo en función del mejor esfuerzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor. Los recursos de cursor se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</p>
<p><strong>JetOpenTempTable3</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host está demasiado fragmentado. El administrador de tablas temporales asignará siempre un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en memoria caché los índices de la tabla. El número de índices cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché el esquema de la tabla. El número de tablas cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para crear una tabla temporal. Los recursos de tabla temporal se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devolverá un cursor abierto en la tabla temporal recién creada. El estado de la base de datos temporal se preparará para contener la nueva tabla temporal. El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.

En caso de error, no se creará la tabla temporal y no se devolverá un cursor. Se puede cambiar el estado de la base de datos temporal. El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.

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

[Errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md)  
[Parámetros de control de errores](./error-handling-parameters.md)  
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
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
