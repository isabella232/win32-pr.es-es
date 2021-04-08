---
description: 'Más información sobre: VistaApi. JetGetInstanceMiscInfo (método)'
title: Método VistaApi. JetGetInstanceMiscInfo (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetGetInstanceMiscInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE@,Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetinstancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 55104187
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 204beee343a717d5b45d8003e123bbbe186437d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908512"
---
# <a name="vistaapijetgetinstancemiscinfo-method"></a>VistaApi. JetGetInstanceMiscInfo, método

Recupera información sobre una instancia de.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetInstanceMiscInfo ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef signature As JET_SIGNATURE, _
    infoLevel As JET_InstanceMiscInfo _
)
'Usage
Dim instance As JET_INSTANCE
Dim signature As JET_SIGNATURE
Dim infoLevel As JET_InstanceMiscInfoVistaApi.JetGetInstanceMiscInfo(instance, _
    signature, infoLevel)
```

``` csharp
public static void JetGetInstanceMiscInfo(
    JET_INSTANCE instance,
    out JET_SIGNATURE signature,
    JET_InstanceMiscInfo infoLevel
)
```

#### <a name="parameters"></a>Parámetros

  - instance  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia de en la que se va a obtener información.

<!-- end list -->

  - firma  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)  
    
    Información recuperada.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)  
    
    Tipo de información que se va a recuperar.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase VistaApi](./vistaapi-class.md)

[Miembros de VistaApi](./vistaapi-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
