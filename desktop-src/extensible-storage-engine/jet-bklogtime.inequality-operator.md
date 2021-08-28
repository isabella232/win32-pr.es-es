---
description: 'Más información sobre: JET_BKLOGTIME. Operador de desigualdad'
title: JET_BKLOGTIME. Operador de desigualdad
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512908
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91a209d0bb3251b536a2facbedc0bb95517eabc689646eb07c512e8ab6560587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781135"
---
# <a name="jet_bklogtimeinequality-operator"></a>JET_BKLOGTIME. Operador de desigualdad

Determina si dos instancias especificadas de JET_BKLOGTIME no son iguales.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a>Parámetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    Primera instancia que se va a comparar.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    Segunda instancia que se va a comparar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si las dos instancias no son iguales.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_BKLOGTIME estructura](./jet-bklogtime-structure2.md)

[JET_BKLOGTIME miembros](./jet-bklogtime-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
