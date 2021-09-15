---
description: Más información sobre el método Server2003Api.JetOSSnapshotAbort
title: Método Server2003Api.JetOSSnapshotAbort (Microsoft.Isam.Esent.Interop.Server2003)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360107"
---
# <a name="server2003apijetossnapshotabort-method"></a>Método Server2003Api.JetOSSnapshotAbort

Notifica al motor que puede reanudar las operaciones normales de E/S una vez finalizado un período de inmovilización con una instantánea con errores.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificador de la sesión de instantánea.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)  
    
    Opciones para esta llamada.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase Server2003Api](./server2003api-class.md)

[Miembros Server2003Api](./server2003api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
