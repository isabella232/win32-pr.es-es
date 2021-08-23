---
description: Más información sobre el método VistaApi.JetOSSnapshotPrepareInstance
title: Método VistaApi.JetOSSnapshotPrepareInstance (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'JetOSSnapshotPrepareInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotprepareinstance(v=EXCHG.10)
ms:contentKeyID: 55104304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9aa33a9d6bf1aec0c5c55844c509ef50b7fe0e31da2db118044d84a4662ccb28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978145"
---
# <a name="vistaapijetossnapshotprepareinstance-method"></a>Método VistaApi.JetOSSnapshotPrepareInstance

Selecciona una instancia específica para formar parte de la sesión de instantánea.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepareInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotPrepareInstanceGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotPrepareInstanceGrbitVistaApi.JetOSSnapshotPrepareInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotPrepareInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotPrepareInstanceGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - instantánea  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificador de instantánea.

<!-- end list -->

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia que se agregará a la instantánea.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)  
    
    Opciones para esta llamada.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[VistaApi (clase)](./vistaapi-class.md)

[Miembros de VistaApi](./vistaapi-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
