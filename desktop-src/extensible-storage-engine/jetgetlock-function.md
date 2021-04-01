---
description: 'Más información acerca de: JetGetLock (función)'
title: JetGetLock función)
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104157280"
---
# <a name="jetgetlock-function"></a>JetGetLock función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetlock-function"></a>JetGetLock función)

La función **JetGetLock** proporciona un medio para reservar explícitamente la capacidad de actualizar una fila, un bloqueo de escritura o impedir explícitamente que una fila se actualice en cualquier otra sesión, bloqueo de lectura. Normalmente, los bloqueos de escritura de filas se adquieren implícitamente como resultado de la actualización de filas. Normalmente, los bloqueos de lectura no son necesarios debido a las versiones de registros. Sin embargo, en algunos casos, una transacción puede desear bloquear explícitamente una fila para aplicar la serialización o asegurarse de que una operación subsiguiente se realizará correctamente en virtud de que ya se han realizado los bloqueos necesarios.

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*sesid*

La sesión que se utilizará para esta llamada.

*TABLEID*

Cursor que se utilizará para esta llamada.

*grbit*

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:

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
<td><p>JET_bitReadLock</p></td>
<td><p>Esta marca hace que se adquiera un bloqueo de lectura en el registro actual. Los bloqueos de lectura son incompatibles con los bloqueos de escritura que ya se encuentran en otras sesiones, pero son compatibles con los bloqueos de lectura retenidos por otras sesiones.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWriteLock</p></td>
<td><p>Esta marca hace que se adquiera un bloqueo de escritura en el registro actual. Los bloqueos de escritura no son compatibles con los bloqueos de lectura o escritura retenidos por otras sesiones, pero son compatibles con los bloqueos de lectura retenidos por la misma sesión.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>El <em>grbit</em> determinado no es JET_bitReadLock ni JET_bitWriteLock. Debe ser una de estas dos marcas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor debe estar en un registro para adquirir un bloqueo. Los bloqueos están siempre en los registros.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Solo las sesiones de una transacción pueden adquirir bloqueos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>El cursor no puede ser de solo lectura y adquirir un bloqueo de escritura.</p></td>
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
<td><p>JET_errTransReadOnly</p></td>
<td><p>La sesión debe tener permisos de escritura para adquirir el bloqueo de escritura.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>El error devuelto cuando se solicita un bloqueo conflictivo.</p></td>
</tr>
</tbody>
</table>


En caso de éxito, la sesión ha adquirido el bloqueo solicitado.

En caso de error, la sesión no ha adquirido el bloqueo solicitado.

#### <a name="remarks"></a>Observaciones

No se pueden adquirir bloqueos de escritura con sesiones o cursores que tengan permisos de solo lectura, aunque la sesión y el cursor no realicen en última instancia una operación de actualización. Tanto la sesión como el cursor deben tener privilegios de escritura para poder adquirir un bloqueo de escritura.

Los bloqueos de lectura y escritura son un medio de bloqueo pesimista. El bloqueo pesimista espera que varias sesiones simultáneas entren en conflicto y adquieran bloqueos de antemano para asegurarse de que sus operaciones se realizan correctamente.

La mayoría de las operaciones serán serializables en virtud de los bloqueos tomados implícitamente. Sin embargo, algunas operaciones no lo serán. Para ilustrar esto, tenga en cuenta las dos transacciones.

T1: R (A), U (B)

T2: R (B), U (A)

El control de versiones de nivel de registro garantiza que cada transacción cuando se ejecute simultáneamente verá los valores originales de A y B. No hay ningún orden de serie de ejecución que pueda producir los mismos resultados para A y B en caso de que los resultados dependan de los datos leídos. Para que la aplicación pueda hacer que esta transacción sea serializable, debe adquirir un bloqueo de lectura explícito en y B en cada transacción cuando se lee el valor.

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
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
