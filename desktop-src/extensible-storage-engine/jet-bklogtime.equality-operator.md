---
description: 'Más información acerca de: JET_BKLOGTIME. Operador de igualdad'
title: JET_BKLOGTIME. Operador de igualdad
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515956
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5a75a1fc55159fc5ea71dba09dc1ed54194b940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697882"
---
# <a name="jet_bklogtimeequality-operator"></a>JET_BKLOGTIME. Operador de igualdad

Determina si dos instancias especificadas de JET_BKLOGTIME son iguales.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a>Parámetros

  - LHS  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    Primera instancia que se va a comparar.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    Segunda instancia que se va a comparar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Estructura de JET_BKLOGTIME](./jet-bklogtime-structure2.md)

[Miembros de JET_BKLOGTIME](./jet-bklogtime-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
