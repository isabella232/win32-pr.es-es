---
description: 'Más información acerca de: propiedad JET_RECSIZE. cbOverhead'
title: Propiedad JET_RECSIZE. cbOverhead (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbOverhead property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cboverhead(v=EXCHG.10)
ms:contentKeyID: 39514763
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbOverhead
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e7318428ef4b50a08a05f5021d293ad1d8d78cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696228"
---
# <a name="jet_recsizecboverhead-property"></a>Propiedad JET_RECSIZE. cbOverhead

Obtiene la sobrecarga de la estructura de registro ESENT para este registro. Esto incluye el tamaño de la clave del registro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property cbOverhead As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbOverhead
```

``` csharp
public long cbOverhead { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Estructura de JET_RECSIZE](./jet-recsize-structure2.md)

[Miembros de JET_RECSIZE](./jet-recsize-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
