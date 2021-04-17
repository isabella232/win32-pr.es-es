---
description: 'Más información acerca de: JetOSSnapshotAbort (función)'
title: JetOSSnapshotAbort función)
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716603"
---
# <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort función)

La función **JetOSSnapshotAbort** notifica al motor de que puede reanudar las operaciones de e/s normales después de que finalice un periodo de inmovilización con una instantánea con errores.

**Windows server 2003:**  **JetOSSnapshotAbort** se incorporó en Windows Server 2003.

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*grbit*

Opciones de esta llamada. Este parámetro se reserva para uso futuro y el único valor válido admitido es 0 (cero).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>La sesión de instantáneas no es válida o el parámetro grbit no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>El identificador de la sesión de instantáneas no es válido.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, finalizará la sesión de instantáneas y se reanudará el comportamiento normal del motor. Se puede iniciar una nueva sesión de instantáneas en un momento posterior.

Si se produce un error en esta función, la sesión de instantáneas no se anulará.

#### <a name="remarks"></a>Observaciones

Se debe llamar a esta función en lugar de a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para informar al motor de que la instantánea se ha anulado por razones que no están relacionadas con el motor. Esta información se puede usar más adelante para ayudar a emitir mensajes de registro de eventos acerca de la sesión de instantáneas o para ayudar a determinar otras acciones adecuadas.

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
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
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
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
