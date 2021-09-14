---
description: 'Más información sobre: JET_COLUMNID. Operador LessThan'
title: JET_COLUMNID. Operador LessThan
TOCTitle: 'LessThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthan(v=EXCHG.10)
ms:contentKeyID: 39512911
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 263cb7be0377da007e6294b29701613628ec692d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126883036"
---
# <a name="jet_columnidlessthan-operator"></a>JET_COLUMNID. Operador LessThan

Determine si un columnid está delante de otro columnid.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator < ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs < rhs)
```

``` csharp
public static bool operator <(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a>Parámetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Primer columnid que se compara.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Segundo columnid que se comparará.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si lhs va antes que rhs.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_COLUMNID estructura](./jet-columnid-structure.md)

[JET_COLUMNID miembros](./jet-columnid-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
