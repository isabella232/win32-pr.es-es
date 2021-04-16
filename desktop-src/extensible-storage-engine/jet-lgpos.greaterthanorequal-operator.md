---
description: 'Más información acerca de: JET_LGPOS. Operador GreaterThanOrEqual'
title: JET_LGPOS. Operador GreaterThanOrEqual
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510730
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a932ea983b3044d1db8395fbf87962cd3b733ae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678540"
---
# <a name="jet_lgposgreaterthanorequal-operator"></a>JET_LGPOS. Operador GreaterThanOrEqual

Determinar si una posición del registro es posterior o igual a otra posición del registro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a>Parámetros

  - LHS  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Primera posición del registro que se va a comparar.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Segunda posición del registro que se va a comparar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True si LHS viene después de o es igual a RHS.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Estructura de JET_LGPOS](./jet-lgpos-structure2.md)

[Miembros de JET_LGPOS](./jet-lgpos-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
