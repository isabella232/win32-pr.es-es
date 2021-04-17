---
description: 'Más información sobre: Server2003Api. JetOSSnapshotAbort (método)'
title: Método Server2003Api. JetOSSnapshotAbort (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: 'JetOSSnapshotAbort method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetossnapshotabort(v=EXCHG.10)
ms:contentKeyID: 55104209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44ee61a7c6cff7fe90a77fdaced786532457c132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696642"
---
# <a name="server2003apijetossnapshotabort-method"></a>Server2003Api. JetOSSnapshotAbort, método

Notifica al motor de que puede reanudar las operaciones de e/s normales después de que finalice un período de inmovilización con una instantánea con errores.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetOSSnapshotAbort ( _
    snapid As JET_OSSNAPID, _
    grbit As SnapshotAbortGrbit _
)
'Usage
Dim snapid As JET_OSSNAPID
Dim grbit As SnapshotAbortGrbitServer2003Api.JetOSSnapshotAbort(snapid, _
    grbit)
```

``` csharp
public static void JetOSSnapshotAbort(
    JET_OSSNAPID snapid,
    SnapshotAbortGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - snapid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificador de la sesión de instantánea.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. Server2003. SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)  
    
    Opciones para esta llamada.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase Server2003Api](./server2003api-class.md)

[Miembros de Server2003Api](./server2003api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
