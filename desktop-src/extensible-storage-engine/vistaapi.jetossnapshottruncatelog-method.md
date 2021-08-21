---
description: Más información sobre el método VistaApi.JetOSSnapshotTruncateLog
title: Método VistaApi.JetOSSnapshotTruncateLog (Microsoft.Isam.Esent.Interop.Vista)
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
ms.openlocfilehash: d216a79934485ed2ea447bd31e93de575e068aa2f548315c2665759aec7a7708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106819"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a>Método VistaApi.JetOSSnapshotTruncateLog

Habilita el truncamiento del registro para todas las instancias que forman parte de la sesión de instantáneas.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificador de instantánea.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)  
    
    Opciones para esta llamada.

## <a name="remarks"></a>Comentarios

Solo se debe llamar a esta función si la instantánea se creó con [la opción ContinueAfterThaw.](./vistagrbits.continueafterthaw-field.md) De lo contrario, la sesión de instantánea finaliza después de la llamada a [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit).](./api.jetossnapshotthaw-method.md)

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[VistaApi (clase)](./vistaapi-class.md)

[Miembros de VistaApi](./vistaapi-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
