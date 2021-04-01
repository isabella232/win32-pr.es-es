---
description: 'Más información sobre: VistaApi. JetOSSnapshotTruncateLogInstance (método)'
title: Método VistaApi. JetOSSnapshotTruncateLogInstance (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75d694629585a730f5c1c7b9b08bb7b06e735cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913746"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a>VistaApi. JetOSSnapshotTruncateLogInstance, método

Trunca el registro de una instancia especificada durante una sesión de instantánea.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - instantánea  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificador de la instantánea.

<!-- end list -->

  - instance  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia para la que se va a truncar el registro.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. vista. SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)  
    
    Opciones para esta llamada.

## <a name="remarks"></a>Observaciones

Solo se debe llamar a esta función si la instantánea se creó con la opción [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) . De lo contrario, la sesión de instantánea finaliza después de la llamada a [JetOSSnapshotThaw (JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase VistaApi](./vistaapi-class.md)

[Miembros de VistaApi](./vistaapi-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
