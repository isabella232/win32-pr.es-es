---
description: 'Más información sobre: API. JetOSSnapshotFreeze (método)'
title: Método API. JetOSSnapshotFreeze
TOCTitle: 'JetOSSnapshotFreeze method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotfreeze(v=EXCHG.10)
ms:contentKeyID: 55100793
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7434cb79e90f99ab946c86a97559079352956fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279085"
---
# <a name="apijetossnapshotfreeze-method"></a>Método API. JetOSSnapshotFreeze

Inicia una instantánea. Mientras la instantánea está en curso, no se puede llevar a cabo ninguna actividad de escritura en disco por parte del motor.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetOSSnapshotFreeze ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotFreezeGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotFreezeGrbitApi.JetOSSnapshotFreeze(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotFreeze(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotFreezeGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - instantánea  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Sesión de la instantánea.

<!-- end list -->

  - numInstances  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Devuelve el número de instancias que forman parte de la sesión de instantáneas.

<!-- end list -->

  - instances  
    Automáticamente \[\]  
    
    Devuelve información sobre las instancias de que forman parte de la sesión de instantáneas.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)  
    
    Opciones de inmovilización de instantáneas.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
