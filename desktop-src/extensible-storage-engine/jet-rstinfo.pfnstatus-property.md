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
ms.openlocfilehash: 57b400e91867d4408fcdb93b979d1a39d8e7eb76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965579"
---
# <a name="jet_rstinfopfnstatus-property"></a>JET_RSTINFO.pfnStatus, propiedad

Obtiene o establece la devolución de llamada en Obtiene o establece la función status.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

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

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_RSTINFO clase](./jet-rstinfo-class.md)

[JET_RSTINFO miembros](./jet-rstinfo-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
