---
description: Más información sobre el método Api.JetOSSnapshotFreeze
title: Método Api.JetOSSnapshotFreeze
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
ms.openlocfilehash: 534f002f785c48ff44a39b4bde4b03733b3d418a5c459fe14b4fb59d074b4f02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978045"
---
# <a name="apijetossnapshotfreeze-method"></a>Método Api.JetOSSnapshotFreeze

Inicia una instantánea. Mientras la instantánea está en curso, el motor no puede realizar ninguna actividad de escritura en disco.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Sesión de instantánea.

<!-- end list -->

  - numInstances  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Devuelve el número de instancias que forman parte de la sesión de instantáneas.

<!-- end list -->

  - instances  
    Tipo: \[\]  
    
    Devuelve información sobre las instancias que forman parte de la sesión de instantánea.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)  
    
    Opciones de inmovilización de instantáneas.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
