---
description: 'Más información sobre: JetOpenTemporaryTable (Función)'
title: JetOpenTemporaryTable (Función)
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e0b0b0ee437e24bd66c8d2f4a8afd178bc4a3ef4b6199434f8da79f50128bf8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944625"
---
# <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable (Función)

La **función JetOpenTemporaryTable** crea una tabla volátil con un único índice que se puede usar para almacenar y recuperar registros, al igual que una tabla normal que se crea a través de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

**Windows Vista:****JetOpenTemporaryTable** se introdujo en Windows Vista.  

Las tablas temporales son más rápidas que las tablas normales debido a su naturaleza volátil. Pueden ordenar y realizar rápidamente la eliminación de duplicados en los conjuntos de registros cuando se accede a ellos de una manera puramente secuencial.

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se usará para esta llamada.

*popentemporarytable*

Puntero a una estructura [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) que contiene la descripción de la tabla temporal que se creará en la entrada. Después de una llamada correcta, la estructura contiene el identificador de la tabla temporal y las identificaciones de columna.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>Error en la operación porque no se pudo asignar suficiente memoria para completarla.</p>
<p><strong>JetOpenTemporaryTable</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host se fragmenta demasiado. El administrador de tablas temporales asignará un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos almacenados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios valores de parámetro dio lugar a un resultado inesperado.</p>
<p><strong>JetOpenTemporaryTable</strong> devuelve este error en las condiciones siguientes:</p>
<ul>
<li><p>El <strong>miembro cbStruct</strong> de la <a href="gg269206(v=exchg.10).md">estructura JET_OPENTEMPORARYTABLE</a> no corresponde a una versión de esta estructura que sea compatible con esa versión del motor de base de datos.</p></li>
<li><p>El <strong>miembro cbKeyMost</strong> de la <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> estructura es menor que JET_cbKeyMostMin.</p></li>
<li><p>El <strong>miembro cbKeyMost</strong> de la <a href="gg269206(v=exchg.10).md">estructura JET_OPENTEMPORARYTABLE</a> es mayor que el mayor valor admitido para el tamaño de página de la base de datos para la instancia (JET_paramDatabasePageSize). Consulte el JET_paramKeyMost en la lista de <a href="gg269241(v=exchg.10).md">parámetros informativos</a> para obtener más información.</p></li>
<li><p>El miembro cbVarSegMac de la <a href="gg269206(v=exchg.10).md">estructura JET_OPENTEMPORARYTABLE</a> es mayor que el <strong>miembro cbKeyMost.</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>La operación no se puede completar porque aún no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>La operación no se puede completar porque la instancia asociada a la sesión ha encontrado un error irrevocado que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>El identificador de sesión no es válido o hace referencia a una sesión cerrada.</p>
<p><strong>Nota</strong>  Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Error en la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor. Los recursos de cursor se configuran <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>Error en la operación porque el motor no puede asignar los recursos necesarios para crear una tabla temporal. Los recursos de tabla temporal se configuran <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> <a href="gg294140(v=exchg.10).md">con JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>Error de JetOpenTemporaryTable</strong> porque JET_bitTTForwardOnly se especificó y no se pudo crear la tabla temporal especificada mediante la optimización de solo avance.</p>
<p><strong>Windows Server 2003:</strong>  Este error solo lo devolverá Windows Server 2003 y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, no más de JET_ccolVarMost columnas de longitud variable y no más de JET_ccolTaggedMost columnas etiquetadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Error en la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché el esquema de la tabla. Para configurar el número de tablas que tienen esquemas que se pueden almacenar en caché, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>El <strong>miembro cp</strong> de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> estructura no se estableció en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (inglés, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>El <strong>miembro coltyp</strong> <a href="gg294130(v=exchg.10).md">del</a> JET_COLUMNDEF no se estableció en un tipo de columna válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>No se pudo crear el índice porque se intentó usar un identificador de configuración regional no válido. Es posible que el identificador de configuración regional no sea completamente válido o que el paquete de idioma asociado no esté instalado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>No se pudo crear el índice porque se intentó usar un conjunto no válido de marcas de normalización.</p>
<p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p>
<p><strong>Windows 2000:</strong>  En Windows 2000, las marcas de normalización no válidas darán lugar a JET_errIndexInvalidDef.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>No se pudo crear el índice porque se especificó una definición de índice no válida. <strong>JetOpenTemporaryTable</strong> devolverá este error en las condiciones siguientes:</p>
<ul>
<li><p>Se especifica la configuración regional idioma neutro.</p></li>
<li><p>Se especifica un conjunto no válido de marcas de normalización.</p></li>
</ul>
<p><strong>Windows 2000:</strong>  Este error solo lo devolverá Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>Error en la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché los índices de la tabla. Para configurar el número de índices que tienen esquemas que se pueden almacenar en caché, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxOpenTables</a>.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devolverá un cursor abierto en la tabla temporal recién creada. El estado de la base de datos temporal se preparará para contener la nueva tabla temporal. El estado de las bases de datos normales en uso por el motor de base de datos permanecerá sin cambios.

En caso de error, no se creará la tabla temporal y no se devolverá un cursor. Se puede cambiar el estado de la base de datos temporal. El estado de las bases de datos normales en uso por el motor de base de datos permanecerá sin cambios.

#### <a name="remarks"></a>Comentarios

Las tablas temporales no admiten el complemento completo de las opciones de definición de columna que normalmente son compatibles con el motor de base de datos. De hecho, solo JET_bitColumnFixed y JET_bitColumnTagged se admiten. Esto significa que no es posible crear una columna de incremento automático, versión o multivalor en una tabla temporal. Por último, las columnas de actualización de custodia no se admiten porque solo las puede usar una sesión a la vez. Si se solicita cualquiera de estas opciones, se omitirán.

Las tablas temporales no admiten valores predeterminados. Si se proporciona una definición de columna que contiene una especificación de valor predeterminado, esa especificación se omitirá.

Las tablas temporales se devuelven al autor de la llamada como resultado de muchas funciones ese diferentes. Por ejemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md) con el conjunto JET_IdxInfo opciones devolverá una tabla temporal que contiene una lista de todas las columnas de clave de un índice determinado. Las tablas temporales siguen las mismas reglas de ciclo de vida que las tablas temporales normales, como se describe aquí.

El motor de base de datos también usa internamente tablas temporales para muchas tareas. La más importante de estas tareas es la creación de un índice sobre una tabla existente. Se usará una tabla temporal para ordenar las claves de índice que se usan para construir ese índice.

Todas las tablas temporales se almacenan en la base de datos temporal. La base de datos temporal es un archivo de base de datos especial que se mantiene durante la vigencia de una instancia de ESE y se elimina cuando esa instancia se cierra o reinicia. La ubicación de la base de datos temporal se puede configurar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) [con JET_paramTempPath](./temporary-database-parameters.md). La ubicación de la base de datos temporal en el disco en relación con los archivos de registro de transacciones y los archivos de base de datos puede ser importante si la aplicación hace un uso pesado de las tablas temporales o crea índices con frecuencia.

El ciclo de vida de una tabla temporal está asociado a los cursores que hacen referencia a ella. Si se cierran todos los cursores que hacen referencia a una tabla temporal, ya sea implícita o explícitamente, se eliminará la tabla temporal. Si se crea una tabla temporal dentro de una transacción y esa transacción se revierte posteriormente, se eliminará la tabla temporal porque los cursores que hacen referencia a ella en este momento se cerrarán implícitamente. Los nuevos cursores pueden hacer referencia a una tabla temporal solo mediante el uso de [JetDupCursor](./jetdupcursor-function.md). En este caso, los nuevos cursores se colocarán en la primera entrada de índice de la tabla temporal. [JetDupCursor](./jetdupcursor-function.md) solo funcionará durante determinadas fases de uso para la tabla temporal. Consulte los comentarios relativos a las funcionalidades de cursor de tabla temporal para obtener más información. No es posible hacer referencia a una tabla temporal de más de una sesión a la vez.

**Precaución**  Hay un problema importante en [JetDupCursor](./jetdupcursor-function.md) que afecta a las tablas temporales. Si se intenta duplicar una tabla temporal que está en modo de solo avance, el cursor resultante no se creará correctamente y no se realizará correctamente. Todavía es seguro duplicar un cursor sobre una tabla temporal materializada.

El administrador de tablas temporales puede implementar una tabla temporal de tres maneras. El primer método consiste en mantener una tabla en memoria. Esta estrategia es la más rápida, pero solo se puede usar para tablas pequeñas, sencillas y temporales. El segundo método consiste en crear una ordenación basada en disco que se pueda basar mediante un iterador de solo avance. Esta estrategia solo se puede usar en determinadas circunstancias y es la manera más rápida de ordenar y quitar duplicados de un conjunto de datos muy grande. El tercer método consiste en crear un árbol B+ en la base de datos temporal para contener la tabla temporal. Esta estrategia es la más lenta, pero la más versátil, y se conoce como tabla temporal materializada. Estas estrategias se pueden usar en combinación para lograr en última instancia la funcionalidad que se solicita de la tabla temporal.

Cuando la tabla temporal no se materializa, se usa principalmente en dos fases principales. La primera fase es la fase de inserción donde la tabla se rellena con su conjunto de datos inicial. Durante esta fase, solo se permite la inserción de datos. Esta fase finaliza cuando se intenta mover el cursor mediante [JetMove](./jetmove-function.md) [o JetSeek](./jetseek-function.md). La segunda fase es la fase de extracción de datos. Durante esta fase, los datos almacenados en la tabla temporal se pueden extraer según las funcionalidades que se solicitaron cuando se creó la tabla temporal.

**Funcionalidades de cursor de tabla temporal**

Cuando se materializa la tabla temporal, el cursor tiene las siguientes funcionalidades, pero puede estar aún más limitado por las opciones que se solicitan:

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

Cuando la tabla temporal no se materializa y se encuentra en la fase de inserción, el cursor tiene las siguientes funcionalidades, pero puede estar aún más limitado por las opciones que se solicitan:

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

Cuando la tabla temporal no se materializa y se encuentra en la fase de extracción, el cursor tiene las siguientes funcionalidades, pero puede estar aún más limitado por las opciones que se solicitan:

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros informativos](./informational-parameters.md)  
[Parámetros temporales de base de datos](./temporary-database-parameters.md)
