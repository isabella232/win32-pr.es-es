---
description: 'Más información sobre: JET_SIGNATURE. Operador de desigualdad'
title: JET_SIGNATURE. Operador de desigualdad
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b0741308777389787f299f377160431dbbd29ca51b368e477fde04dc54337f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118253031"
---
# <a name="jet_signatureinequality-operator"></a>JET_SIGNATURE. Operador de desigualdad

Determina si dos instancias especificadas de JET_SIGNATURE no son iguales.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a>Parámetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)  
    
    Primera instancia que se va a comparar.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)  
    
    Segunda instancia que se va a comparar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si las dos instancias no son iguales.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_SIGNATURE estructura](./jet-signature-structure2.md)

[JET_SIGNATURE miembros](./jet-signature-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
