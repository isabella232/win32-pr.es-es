---
description: 'Más información sobre: JET_RSTINFO.pfnStatus'
title: JET_RSTINFO.pfnStatus, propiedad
TOCTitle: 'pfnStatus property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.pfnstatus(v=EXCHG.10)
ms:contentKeyID: 55103829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.set_pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.get_pfnStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a4a74518b50358dc2e6317009684db356562d54927012c6af433f4172bd4f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967598"
---
# <a name="jet_rstinfopfnstatus-property"></a>JET_RSTINFO.pfnStatus, propiedad

Obtiene o establece la devolución de llamada en Obtiene o establece la función status.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pfnStatus As JET_PFNSTATUS
    Get
    Set
'Usage
Dim instance As JET_RSTINFO
Dim value As JET_PFNSTATUS

value = instance.pfnStatus

instance.pfnStatus = value
```

``` csharp
public JET_PFNSTATUS pfnStatus { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_RSTINFO clase](./jet-rstinfo-class.md)

[JET_RSTINFO miembros](./jet-rstinfo-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
