---
description: 'Más información acerca de: JET_LOGTIME. Operador de igualdad'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697880"
---
# <a name="jet_logtimeequality-operator"></a>JET_LOGTIME. Operador de igualdad

Determina si dos instancias especificadas de JET_LOGTIME son iguales.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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

  - LHS  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  
    
    Primera instancia que se va a comparar.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  
    
    Segunda instancia que se va a comparar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Estructura de JET_LOGTIME](./jet-logtime-structure2.md)

[Miembros de JET_LOGTIME](./jet-logtime-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
