---
description: 'Más información acerca de: JET_COLUMNID. Operador de desigualdad'
title: JET_COLUMNID. Operador de desigualdad
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516136
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b6b0856a5c551be06dd7f4b55f8f144c0e509f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706519"
---
# <a name="jet_columnidinequality-operator"></a>JET_COLUMNID. Operador de desigualdad

Determina si dos instancias especificadas de JET_COLUMNID no son iguales.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a>Parámetros

  - LHS  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Primera instancia que se va a comparar.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Segunda instancia que se va a comparar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True si las dos instancias de no son iguales.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Estructura de JET_COLUMNID](./jet-columnid-structure.md)

[Miembros de JET_COLUMNID](./jet-columnid-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
