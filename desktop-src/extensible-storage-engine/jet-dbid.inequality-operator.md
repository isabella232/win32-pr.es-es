---
description: 'Más información sobre: JET_DBID. Operador de desigualdad'
title: JET_DBID. Operador de desigualdad
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_DBID.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04a6ac55d1768eaf29146d89bf69be4cbcf90fd7686590153432533e7bff5684
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017345"
---
# <a name="jet_dbidinequality-operator"></a>JET_DBID. Operador de desigualdad

Determina si dos instancias especificadas de JET_DBID no son iguales.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_DBID, _
    rhs As JET_DBID _
) As Boolean
'Usage
Dim lhs As JET_DBID
Dim rhs As JET_DBID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_DBID lhs,
    JET_DBID rhs
)
```

#### <a name="parameters"></a>Parámetros

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Primera instancia que se va a comparar.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Segunda instancia que se va a comparar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si las dos instancias no son iguales.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_DBID estructura](./jet-dbid-structure.md)

[JET_DBID miembros](./jet-dbid-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
