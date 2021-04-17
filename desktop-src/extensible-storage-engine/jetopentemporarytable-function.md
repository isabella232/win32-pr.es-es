---
description: 'Más información acerca de: JetOpenTemporaryTable (función)'
title: JetOpenTemporaryTable función)
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
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697443"
---
# <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable función)

La función **JetOpenTemporaryTable** crea una tabla volátil con un índice único que se puede usar para almacenar y recuperar registros, al igual que una tabla normal que se crea a través de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

**Windows Vista:**  **JetOpenTemporaryTable** se presentó en Windows Vista.

Las tablas temporales son más rápidas que las normales debido a su naturaleza volátil. Pueden ordenar y realizar rápidamente la eliminación de duplicados en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

La sesión que se utilizará para esta llamada.

*popentemporarytable*

Puntero a una estructura de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) que contiene la descripción de la tabla temporal que se va a crear en la entrada. Después de una llamada correcta, la estructura contiene el identificador de la tabla temporal y las identificaciones de las columnas.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</p>
<p><strong>JetOpenTemporaryTable</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host está demasiado fragmentado. El administrador de tablas temporales asignará un fragmento de espacio de direcciones de 1 MB para cada tabla temporal creada independientemente de la cantidad de datos que se almacenen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado.</p>
<p>Este error lo devuelve <strong>JetOpenTemporaryTable</strong> en las siguientes condiciones:</p>
<ul>
<li><p>El miembro <strong>cbStruct</strong> de la estructura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> no se corresponde con una versión de esta estructura compatible con esa versión del motor de base de datos.</p></li>
<li><p>El miembro <strong>cbKeyMost</strong> de la estructura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> es menor que JET_cbKeyMostMin.</p></li>
<li><p>El miembro <strong>cbKeyMost</strong> de la estructura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> es mayor que el mayor valor admitido para el tamaño de página de la base de datos de la instancia (JET_paramDatabasePageSize). Vea el parámetro JET_paramKeyMost en la lista de <a href="gg269241(v=exchg.10).md">parámetros informativos</a> para obtener más información.</p></li>
<li><p>El miembro cbVarSegMac de la estructura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> es mayor que el miembro <strong>cbKeyMost</strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia que estaba asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>El identificador de sesión no es válido o hace referencia a una sesión cerrada.</p>
<p><strong>Nota:</strong>  Este error no se devuelve en todas las circunstancias. Los identificadores se validan solo en función del mejor esfuerzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor. Los recursos de cursor se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para crear una tabla temporal. Los recursos de tabla temporal se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p>Error de <strong>JetOpenTemporaryTable</strong> porque se especificó JET_bitTTForwardOnly y no se pudo crear la tabla temporal que se especificó mediante la optimización de solo avance.</p>
<p><strong>Windows Server 2003:</strong>  Este error solo lo devolverán Windows Server 2003 y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché el esquema de la tabla. Para configurar el número de tablas que tienen esquemas que se pueden almacenar en caché, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>El miembro <strong>CP</strong> de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>El miembro <strong>coltyp</strong> de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en un tipo de columna válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>No se pudo crear el índice porque se intentó usar un ID. de configuración regional no válido. Es posible que el ID. de configuración regional no sea válido o que el paquete de idioma asociado no esté instalado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>No se pudo crear el índice porque se intentó usar un conjunto no válido de marcas de normalización.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p>
<p><strong>Windows 2000:</strong>  En Windows 2000, las marcas de normalización no válidas producirán JET_errIndexInvalidDef.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>No se pudo crear el índice porque se especificó una definición de índice no válida. <strong>JetOpenTemporaryTable</strong> devolverá este error en las siguientes condiciones:</p>
<ul>
<li><p>Se especifica la configuración regional independiente del idioma.</p></li>
<li><p>Se especifica un conjunto no válido de marcas de normalización.</p></li>
</ul>
<p><strong>Windows 2000:</strong>  Este error solo lo devolverá Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en memoria caché los índices de la tabla. Para configurar el número de índices que tienen esquemas que se pueden almacenar en caché, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devolverá un cursor abierto en la tabla temporal recién creada. El estado de la base de datos temporal se preparará para contener la nueva tabla temporal. El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.

En caso de error, no se creará la tabla temporal y no se devolverá un cursor. Se puede cambiar el estado de la base de datos temporal. El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.

#### <a name="remarks"></a>Observaciones

Las tablas temporales no admiten el complemento completo de las opciones de definición de columna que normalmente admite el motor de base de datos. De hecho, solo se admiten JET_bitColumnFixed y JET_bitColumnTagged. Esto significa que no es posible crear una columna de incremento automático, versión o multivalor en una tabla temporal. Por último, no se admiten las columnas de actualización de custodia porque solo se pueden usar en una sesión a la vez. Si se solicita alguna de estas opciones, se omitirán.

Las tablas temporales no admiten valores predeterminados. Si se proporciona una definición de columna que contiene una especificación de valor predeterminado, se omitirá esa especificación.

Las tablas temporales se devuelven al autor de la llamada como resultado de muchas funciones de ESE diferentes. Por ejemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md) con el conjunto de opciones JET_IdxInfo devolverá una tabla temporal que contenga una lista de todas las columnas de clave de un índice determinado. Las tablas temporales siguen las mismas reglas del ciclo de vida que las tablas temporales normales, como se describe aquí.

El motor de base de datos también usa internamente las tablas temporales para muchas tareas. Lo más importante de estas tareas es la creación de un índice en una tabla existente. Se utilizará una tabla temporal para ordenar las claves de índice que se usan para construir ese índice.

Todas las tablas temporales se almacenan en la base de datos temporal. La base de datos temporal es un archivo de base de datos Especial que se mantiene durante la vigencia de una instancia de ESE y se elimina cuando se cierra o se reinicia la instancia. La ubicación de la base de datos temporal se puede configurar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramTempPath](./temporary-database-parameters.md). La selección de ubicación de la base de datos temporal en el disco en relación con los archivos de registro de transacciones y los archivos de base de datos puede ser importante si la aplicación hace un uso intensivo de tablas temporales o crea índices con frecuencia.

El ciclo de vida de una tabla temporal está asociado a los cursores que hacen referencia a él. Si se cierran todos los cursores que hacen referencia a una tabla temporal, ya sea implícita o explícitamente, se eliminará la tabla temporal. Si una tabla temporal se crea dentro de una transacción y esa transacción se revierte posteriormente, se eliminará la tabla temporal, ya que todos los cursores que hagan referencia a ella en este momento se cerrarán implícitamente. Los nuevos cursores solo pueden hacer referencia a una tabla temporal mediante el uso de [JetDupCursor](./jetdupcursor-function.md). En este caso, los nuevos cursores se colocarán en la primera entrada de índice de la tabla temporal. [JetDupCursor](./jetdupcursor-function.md) solo funcionará durante ciertas fases de uso de la tabla temporal. Para obtener más información, consulte las notas sobre las funcionalidades de cursor de tabla temporal. No es posible hacer referencia a una tabla temporal de más de una sesión a la vez.

**PRECAUCIÓN**  Hay un problema importante en [JetDupCursor](./jetdupcursor-function.md) que afecta a las tablas temporales. Si se realiza un intento de duplicar una tabla temporal que está en modo de solo avance, el cursor resultante no se creará correctamente y dejará de funcionar. Todavía es seguro duplicar un cursor sobre una tabla temporal materializada.

El administrador de tablas temporales puede implementar una tabla temporal de tres maneras. El primer método consiste en mantener una tabla en memoria. Esta estrategia es la más rápida, pero solo se puede usar para tablas pequeñas, simples y temporales. El segundo método consiste en crear una ordenación basada en disco que se puede controlar mediante un iterador de solo avance. Esta estrategia solo se puede usar en determinadas circunstancias y es la manera más rápida de ordenar y quitar duplicados de un conjunto de datos muy grande. El tercer método consiste en crear un árbol B + en la base de datos temporal para almacenar la tabla temporal. Esta estrategia es la más lenta, pero la más versátil, y se conoce como una tabla temporal materializada. Estas estrategias se pueden usar en combinación para lograr en última instancia la funcionalidad solicitada de la tabla temporal.

Cuando la tabla temporal no se materializa, se usa principalmente en dos fases principales. La primera fase es la fase de inserción en la que la tabla se rellena con su conjunto de datos inicial. Durante esta fase, solo se permite la inserción de datos. Esta fase finaliza cuando se realiza un intento de trasladar el cursor mediante [JetMove](./jetmove-function.md) o [JetSeek](./jetseek-function.md). La segunda fase es la fase de extracción de datos. Durante esta fase, los datos que se almacenan en la tabla temporal se pueden extraer según las capacidades que se solicitaron cuando se creó la tabla temporal.

**Funciones de cursor de tabla temporal**

Cuando se materializa la tabla temporal, el cursor tiene las siguientes capacidades, pero puede estar más limitado por las opciones que se solicitan:

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

Cuando la tabla temporal no se materializa y se encuentra en la fase de inserción, el cursor tiene las siguientes capacidades, pero puede estar más limitado por las opciones que se solicitan:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)
    
    **Nota:**  Provoca la transición a la fase de extracción.

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)
    
    **Nota:**  Provoca la transición a la fase de extracción.

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetUpdate](./jetupdate-function.md)

Cuando la tabla temporal no se materializa y se encuentra en la fase de extracción, el cursor tiene las siguientes capacidades, pero puede estar más limitado por las opciones que se solicitan:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)
    
    **Nota:**  Si se realiza un intento de duplicar una tabla temporal que está en modo de solo avance, el cursor resultante no se creará correctamente y dejará de funcionar. Todavía es seguro duplicar un cursor sobre una tabla temporal materializada.

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
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
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
