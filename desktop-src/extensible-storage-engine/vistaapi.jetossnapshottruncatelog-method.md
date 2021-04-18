---
description: 'Más información sobre: VistaApi. JetOSSnapshotTruncateLog (método)'
title: Método VistaApi. JetOSSnapshotTruncateLog (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOSSnapshotTruncateLog method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncatelog(v=EXCHG.10)
ms:contentKeyID: 55104308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0af8054bc414ea5dbd6c7225fa9e2cd7117c74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686474"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a>VistaApi. JetOSSnapshotTruncateLog, método

Habilita el truncamiento del registro para todas las instancias que forman parte de la sesión de instantáneas.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLog ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLog(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLog(
    JET_OSSNAPID snapshot,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - instantánea  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificador de la instantánea.

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
