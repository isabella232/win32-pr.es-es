---
description: 'Más información acerca de: JetEscrowUpdate (función)'
title: Función JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706889"
---
# <a name="jetescrowupdate-function"></a>Función JetEscrowUpdate


_**Se aplica a:** Windows | Windows Server_

## <a name="jetescrowupdate-function"></a>Función JetEscrowUpdate

La función **JetEscrowUpdate** realiza una operación de suma atómica en una columna. Esta función permite que varias sesiones actualicen el mismo registro simultáneamente sin conflictos.

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*columnid*

*Columnid* de la columna que se va a actualizar.

*FV*

Un puntero a un búfer que contiene el addend de la columna.

*cbMax*

Tamaño del búfer que contiene el addend.

*pvOld*

Búfer de salida que recibirá el valor actual de la columna tal y como se almacena en la base de datos (se omite el control de versiones).

*cbOldMax*

Tamaño máximo del búfer de salida que recibirá el valor actual de la columna. Actualmente solo se admite JET_coltypLong, por lo que el búfer debe tener 4 bytes o tener una longitud de 0 bytes. Si *pvOld* es null, *cbOldMax* debe ser 0.

*pcbOldActual*

Recibe la cantidad real de datos de valor sin formato recibidos en el búfer de salida.

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
<td><p>JET_bitEscrowNoRollback</p></td>
<td><p>Incluso si la sesión que realiza la actualización de custodia tiene la reversión de la transacción, esta actualización no se deshará. Tenga en cuenta que, dado que es posible que las entradas de registro no se vacíen en el disco, es posible que se pierdan actualizaciones recientes de custodia realizadas con esta marca si se produce un bloqueo.</p></td>
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
<td><p>JET_errAlreadyPrepared</p></td>
<td><p>El cursor tiene una actualización preparada con <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Se ha pasado un tamaño de búfer no válido. Actualmente solo se admite JET_coltypLong, por lo que el búfer debe ser de 4 bytes.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p>Se ha especificado una columna no válida. La columna se debe crear con JET_bitColumnEscrowUpdate especificado. Solo las columnas fijas de JET_coltypLong pueden especificarse como de actualización de custodia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor debe estar en un registro para actualizar una columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Las actualizaciones de custodia solo las pueden realizar sesiones en una transacción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>El cursor no puede ser de solo lectura y actualizar un registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión desde más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La sesión debe tener permisos de escritura para actualizar un registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>El error devuelto cuando se solicita una actualización en conflicto.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Normalmente, si dos sesiones intentan actualizar un registro simultáneamente, la segunda sesión recibirá un error JET_errWriteConflict a menos que las sesiones se serialicen por completo. Para serializar dos sesiones que actualizan el mismo registro, la segunda sesión debe iniciar su transacción después de que la primera transacción confirme su transacción. Vea [JetBeginTransaction](./jetbegintransaction-function.md) para obtener más información.

Se pueden actualizar varias columnas en el mismo registro. Las actualizaciones no se ven afectadas.

Solo las operaciones **JetEscrowUpdate** son compatibles entre sí. Si dos sesiones diferentes intentan preparar las actualizaciones o eliminar el mismo registro, se generará un conflicto de escritura.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p>Sesión B<br />
<strong>JetEscrowUpdate</strong></p></th>
<th><p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p></th>
<th><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>JetEscrowUpdate</strong></p></td>
<td><p>JET_errSuccess</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="odd">
<td><p>Sesión A</p></td>
<td><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
</tbody>
</table>


Las versiones de las operaciones de custodia se controlan y se deshacen con [JetRollback](./jetrollback-function.md) (a menos que se especifique JET_bitEscrowNoRollback). **JetEscrowUpdate** devuelve el valor sin formato de la columna almacenada en la base de datos, porque una aplicación puede querer realizar una acción especial cuando se alcanza un valor de centinela. [JetRetrieveColumn](./jetretrievecolumn-function.md) devuelve la vista con versión correcta de la columna, omitiendo las actualizaciones realizadas por las sesiones simultáneas.

Dadas dos sesiones que operan en la misma columna del mismo registro, podemos ver cómo funciona esto. Suponga que la columna comienza con un valor de 0.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sesión</p></th>
<th><p>Operación</p></th>
<th><p>Valor almacenado</p></th>
<th><p>Valor devuelto</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>A</p></td>
<td><p><strong>JetEscrowUpdate</strong> (4)</p></td>
<td><p>4</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><strong>JetEscrowUpdate</strong> (3)</p></td>
<td><p>7</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p>A</p></td>
<td><p><strong>JetEscrowUpdate</strong> (2)</p></td>
<td><p>9</p></td>
<td><p>7</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><strong>JetEscrowUpdate</strong> (-7)</p></td>
<td><p>2</p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p>N</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269273(v=exchg.10).md">JetRollback</a></p></td>
<td><p>-1</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
</tbody>
</table>


No se recomienda reemplazar un registro de la misma transacción que realiza actualizaciones de custodia a un registro. En concreto, si se prepara una actualización en un registro con una [JET_TABLEID](./jet-tableid.md) y se usa otro [JET_TABLEID](./jet-tableid.md) para la custodia de la actualización del registro, se perderá el custodia actualizado cuando se llame a [JetUpdate](./jetupdate-function.md) . Esto sucede incluso si la columna custodia no se estableció durante la actualización.

Cuando una columna actualizable de custodia tiene un valor de cero, se puede desencadenar un comportamiento especial. Este comportamiento solo se produce si una operación **JetEscrowUpdate** hace que la columna tenga un valor de cero. La acción no se realiza inmediatamente, pero se produce una vez después de la transacción que hizo que la columna tenga un valor de cero confirmaciones. La columna debe tener todavía un valor de cero (es decir, si ninguna otra sesión ha modificado la columna). Si la columna se creó con JET_bitColumnDeleteOnZero, se eliminará el registro que contiene la columna. Si la columna se creó con JET_bitColumnFinalize, se emitirá una devolución de llamada. Un bloqueo puede hacer que estas acciones no ocurran, pero el mantenimiento en línea (mediante la función [JetDefragment](./jetdefragment-function.md) ) rehará correctamente las acciones.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
