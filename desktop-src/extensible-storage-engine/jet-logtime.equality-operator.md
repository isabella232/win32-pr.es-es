---
description: 'Más información sobre: JET_LOGTIME. Operador de igualdad'
title: JET_LOGTIME. Operador de igualdad
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_LOGTIME,Microsoft.Isam.Esent.Interop.JET_LOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39514101
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f346a1331200b18c2fc9e51d8eebc1ddaef105
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242222"
---
# <a name="jet_logtimeequality-operator"></a>JET_LOGTIME. Operador de igualdad

Determina si dos instancias especificadas de JET_LOGTIME son iguales.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LOGTIME, _
    rhs As JET_LOGTIME _
) As Boolean
'Usage
Dim lhs As JET_LOGTIME
Dim rhs As JET_LOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LOGTIME lhs,
    JET_LOGTIME rhs
)
```

#### <a name="parameters"></a>Parámetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  
    
    Primera instancia que se va a comparar.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  
    
    Segunda instancia que se va a comparar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_LOGTIME estructura](./jet-logtime-structure2.md)

[JET_LOGTIME miembros](./jet-logtime-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
