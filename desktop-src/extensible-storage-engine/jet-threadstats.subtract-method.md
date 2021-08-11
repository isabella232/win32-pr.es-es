---
description: 'Más información sobre: JET_THREADSTATS. Método Subtract'
title: JET_THREADSTATS. Método Subtract (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.subtract(v=EXCHG.10)
ms:contentKeyID: 39514465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 443e572afd80b3af28e2a88f84880e8679e8e462b0a7f7540e4a277cfa759941
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251774"
---
# <a name="jet_threadstatssubtract-method"></a>JET_THREADSTATS. Método Subtract

Calcule la diferencia en las estadísticas entre dos JET_THREADSTATS estructura.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function Subtract ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Subtract(t1, t2)
```

``` csharp
public static JET_THREADSTATS Subtract(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a>Parámetros

  - t1  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    El primer JET_THREADSTATS.

<!-- end list -->

  - t2  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    La segunda JET_THREADSTATS.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Un JET_THREADSTATS que contiene la diferencia en las estadísticas entre t1 y t2.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_THREADSTATS estructura](./jet-threadstats-structure2.md)

[JET_THREADSTATS miembros](./jet-threadstats-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
