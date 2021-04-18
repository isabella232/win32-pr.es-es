---
description: 'Más información acerca de: propiedad JET_DBINFOMISC. bkinfoDiffPrev'
title: Propiedad JET_DBINFOMISC. bkinfoDiffPrev
TOCTitle: 'bkinfoDiffPrev property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.bkinfodiffprev(v=EXCHG.10)
ms:contentKeyID: 39513441
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_bkinfoDiffPrev
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd152d1dffbc4cf956129dfd886186dda0b33084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705581"
---
# <a name="jet_dbinfomiscbkinfodiffprev-property"></a>Propiedad JET_DBINFOMISC. bkinfoDiffPrev

Obtiene información acerca de la última copia de seguridad diferencial correcta. Restablecer cuando se establece [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) .

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property bkinfoDiffPrev As JET_BKINFO
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_BKINFO

value = instance.bkinfoDiffPrev
```

``` csharp
public JET_BKINFO bkinfoDiffPrev { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.ISAM.esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_DBINFOMISC (clase)](./jet-dbinfomisc-class.md)

[Miembros de JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
