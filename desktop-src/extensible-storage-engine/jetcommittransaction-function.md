---
description: 'Más información acerca de: JetCommitTransaction (función)'
title: Función JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002895"
---
# <a name="jetcommittransaction-function"></a>Función JetCommitTransaction


_**Se aplica a:** Windows | Windows Server_

## <a name="jetcommittransaction-function"></a>Función JetCommitTransaction

La función **JetCommitTransaction** confirma los cambios realizados en el estado de la base de datos durante el punto de almacenamiento actual y los migra al punto de almacenamiento anterior. Si se confirma el punto de almacenamiento más externo, los cambios realizados durante ese punto de almacenamiento se confirmarán en el estado de la base de datos y la sesión finalizará la transacción.

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

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
<td><p>JET_bitCommitLazyFlush</p></td>
<td><p>La transacción se confirma normalmente, pero esta API no espera a que la transacción se vacíe en el archivo de registro de transacciones antes de volver al autor de la llamada. Esto reduce drásticamente la duración de una operación de confirmación a costa de la durabilidad. Cualquier transacción que no se vacíe en el registro antes de un bloqueo se anulará automáticamente durante la recuperación tras el bloqueo durante la siguiente llamada a <a href="gg294068(v=exchg.10).md">JetInit</a>.</p>
<p>Si se especifican JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit, se omite esta opción.</p>
<p>Si esta llamada a <strong>JetCommitTransaction</strong> no coincide con la primera llamada a <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> para esta sesión, se omitirá esta opción. Esto se debe a que la acción final que se produce en el punto de almacenamiento más externo es el factor determinante de si toda la transacción se confirma realmente en el disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWaitAllLevel0Commit</p></td>
<td><p>Todas las transacciones confirmadas previamente por cualquier sesión que todavía no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente. Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</p>
<p>Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</p>
<p>Esta opción no se puede usar en combinación con ninguna otra opción.</p>
<p>Esta opción solo está disponible en Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitWaitLastLevel0Commit</p></td>
<td><p>Si la sesión ha confirmado previamente alguna transacción y aún no se ha vaciado en el archivo de registro de transacciones, se deben vaciar inmediatamente. Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada. Esto resulta útil si la aplicación ha confirmado previamente varias transacciones mediante JET_bitCommitLazyFlush y ahora desea vaciar todas ellas en el disco.</p>
<p>Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</p>
<p>Esta opción no se puede usar en combinación con ninguna otra opción.</p></td>
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
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida o no se implementó. Este error lo devolverá <strong>JetCommitTransaction</strong> cuando:</p>
<ul>
<li><p>Se ha especificado un <em>grbit</em> no válido.</p></li>
<li><p>Se especificó JET_bitWaitLastLevel0Commit en combinación con otro <em>grbit</em>.</p></li>
<li><p>Se especificó JET_bitWaitAllLevel0Commit en combinación con otro <em>grbit</em>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>No se pudo realizar la operación porque la sesión especificada no está en una transacción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se confirmarán los cambios realizados en la base de datos durante el punto de almacenamiento actual para la sesión dada y se finalizará el punto de almacenamiento. Si finalizó el último punto de retorno de la sesión, la transacción se vaciará opcionalmente en el archivo de registro de transacciones y la sesión finalizará la transacción.

En caso de error, el estado transaccional de la sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos. La aplicación debe llamar a [JetRollback](./jetrollback-function.md) para anular la transacción.

#### <a name="remarks"></a>Observaciones

Debe haber una llamada a **JetCommitTransaction** o [JetRollback](./jetrollback-function.md) para que coincida con cada llamada a [JetBeginTransaction](./jetbegintransaction-function.md) para una sesión determinada.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction]()  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
