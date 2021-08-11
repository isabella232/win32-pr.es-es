---
description: 'Más información sobre: Función JetCommitTransaction2'
title: Función JetCommitTransaction2
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 697a3760dc3312230bb2fe755dbfc881c1fdbacd7d21c98e64d8aa83a271ecdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251377"
---
# <a name="jetcommittransaction2-function"></a>Función JetCommitTransaction2


_**Se aplica a:** Windows | Windows Servidor_

La **función JetCommitTransaction2** confirma los cambios realizados en el estado de la base de datos durante el punto de guardado actual y los migra al punto de guardado anterior. Si se confirma el punto de guardado más externo, los cambios realizados durante ese punto de guardado se confirman en el estado de la base de datos y la sesión sale de la transacción.

La **función JetCommitTransaction2** se introdujo en el Windows 8 operativo.

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*grbit*

Grupo de bits que especifican cero o más de los valores enumerados en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitCommitLazyFlush</p></td>
<td><p>La transacción se confirma normalmente, pero esta API no espera a que la transacción se vacíe en el archivo de registro de transacciones antes de volver al autor de la llamada. Esto reduce drásticamente la duración de una operación de confirmación a costa de la durabilidad. Cualquier transacción que no se vacíe en el registro antes de un bloqueo se anulará automáticamente durante la recuperación de bloqueos durante la siguiente llamada a la <a href="gg294068(v=exchg.10).md">función JetInit.</a></p>
<p>Si JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit se especifican, se omite esta opción.</p>
<p>Si esta llamada a <strong>JetCommitTransaction2</strong> no coincide con la primera llamada a la función <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> de esta sesión, se omite esta opción. Esto se debe a que la acción final que se produce en el punto de guardado más externo es el factor determinante para determinar si toda la transacción se confirma realmente en el disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWaitAllLevel0Commit</p></td>
<td><p>Todas las transacciones confirmadas previamente por cualquier sesión que aún no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente. Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</p>
<p>Esta opción se puede usar incluso si la sesión no está actualmente en una transacción.</p>
<p>Esta opción no se puede usar en combinación con ninguna otra opción.</p>
<p>Esta opción está disponible en versiones del sistema operativo Windows Server a partir de Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitWaitLastLevel0Commit</p></td>
<td><p>Si la sesión ha confirmado previamente las transacciones y aún no se han vaciado en el archivo de registro de transacciones, se deben vaciar inmediatamente. Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada. Esto resulta útil si la aplicación ha confirmado previamente varias transacciones mediante JET_bitCommitLazyFlush y ahora quiere vaciar todas ellas en el disco.</p>
<p>Esta opción se puede usar incluso si la sesión no está actualmente en una transacción.</p>
<p>Esta opción no se puede usar en combinación con ninguna otra opción.</p></td>
</tr>
</tbody>
</table>


*cmsecDurableCommit*

Duración para confirmar una transacción diferida.

*pCommitID*

Identificador de confirmación asociado a este registro de confirmación.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores extensibles Storage Engine (ESE), vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a la <a href="gg269240(v=exchg.10).md">función JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p>Este error solo lo devolverán las versiones del sistema operativo Windows a partir de Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida o no se implementó. La función <strong>JetCommitTransaction2</strong> devolverá este error cuando se produzca lo siguiente:</p>
<ul>
<li><p>Se especifica <em>un grbit</em> no es así.</p></li>
<li><p>JET_bitWaitLastLevel0Commit se especificó en combinación con otro <em>grbit</em>.</p></li>
<li><p>JET_bitWaitAllLevel0Commit se especificó en combinación con otro <em>grbit</em>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Error en la operación porque la sesión dada no está en una transacción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p>Este error solo lo devolverán las versiones del sistema operativo Windows a partir de Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se realiza correctamente, se confirman los cambios realizados en la base de datos durante el punto de guardado actual de la sesión determinada y se finalizará ese punto de guardado. Si finalizó el último punto de guardado de la sesión, la transacción se vaciará opcionalmente en el archivo de registro de transacciones y la sesión cerrará la transacción.

En caso de error, el estado transaccional de la sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos. La aplicación debe llamar a la [función JetRollback](./jetrollback-function.md) para anular la transacción.

#### <a name="remarks"></a>Comentarios

Debe haber una llamada a **JetCommitTransaction2** o [JetRollback](./jetrollback-function.md) para que coincida con cada llamada a [JetBeginTransaction](./jetbegintransaction-function.md) para una sesión determinada.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2012.</p></td>
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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
