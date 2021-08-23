---
description: 'Más información sobre: operador JET_COMMIT_ID.Inequality'
title: JET_COMMIT_ID.Inequality (Operador) (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Inequality(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_inequality(v=EXCHG.10)
ms:contentKeyID: 55104411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Inequality
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c2891e6d7fa826edccbdf85e2c5b9d284a2a4f9699db179622c4c45459bec112
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834035"
---
# <a name="jet_commit_idinequality-operator"></a>JET_COMMIT_ID.Inequality (Operador)

Determine si un commitid no es igual a otro commitid.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a>Parámetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Primer commitid que se compara.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Segundo commitid que se compara.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si lhs comes no es igual a rhs.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_COMMIT_ID clase](./jet-commit-id-class.md)

[JET_COMMIT_ID miembros](./jet-commit-id-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
