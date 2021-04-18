---
description: 'Más información acerca de: JetGetCursorInfo (función)'
title: JetGetCursorInfo función)
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659992"
---
# <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo función)

La función **JetGetCursorInfo** se usa para determinar si una actualización del registro actual de un cursor producirá un conflicto de escritura, según el estado actual de actualización del registro. Es posible que se devuelva un conflicto de escritura en última instancia, incluso si **JetGetCursorInfo** devuelve JET_errSuccess, porque otra sesión puede actualizar el registro antes de que la sesión actual pueda actualizar el mismo registro.

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

La sesión que se utilizará para esta llamada.

*TABLEID*

Cursor que se utilizará para esta llamada.

*pvResult*

Reservado para uso futuro.

*cbMax*

Debe establecerse en 0 (cero); de lo contrario, no se utiliza. Está presente para futuras funciones.

*InfoLevel*

Debe establecerse en 0 (cero); de lo contrario, no se utiliza. Está presente para futuras funciones.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p><em>CbMax</em> no es 0 (cero) o <em>InfoLevel</em> no es 0 (cero).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está actualmente en un registro y no se puede devolver información sobre un registro lógico como resultado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
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
<td><p>JET_errWriteConflict</p></td>
<td><p>El registro actual del cursor se ha actualizado en otra sesión y una actualización de este registro en esta sesión producirá un conflicto de escritura.</p></td>
</tr>
</tbody>
</table>


Si se realiza correctamente, esta operación no tiene ningún efecto en la ubicación del cursor, pero solo indica que ninguna otra sesión actualizó actualmente este registro.

En caso de error, si se devuelve un código de error negativo, no se produce ningún efecto en el cursor o en la base de datos.

#### <a name="remarks"></a>Observaciones

Esta operación no afecta al estado del cursor o de los datos. Solo devuelve un código de error que describe si se sabe que una actualización del registro actual por la sesión que realiza la llamada da como resultado un JET_errWriteConflict, o se desconoce para devolver JET_errWriteConflict. Si otra sesión ya ha actualizado este registro para usarlo, está seguro de que una actualización de este registro en esta sesión producirá un conflicto de escritura. Esto será así hasta que esta sesión se confirme o revierta sus transacciones al nivel de transacción 0 (cero). Sin embargo, si **JetGetCursorInfo** devuelve JET_errSuccess, sigue siendo posible que otra sesión actualice este registro antes de la sesión actual y, por lo tanto, siga siendo posible que una actualización del registro actual por esta sesión en su transacción actual produzca un conflicto de escritura.

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

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLock](./jetgetlock-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
