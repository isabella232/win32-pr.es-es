---
description: 'Más información acerca de: JET_THREADSTATS. Add (método)'
title: JET_THREADSTATS. Método Add (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.add(v=EXCHG.10)
ms:contentKeyID: 39514259
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2a824249fde43de92c65d64d02fbab4097b7dc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705455"
---
# <a name="jet_threadstatsadd-method"></a>JET_THREADSTATS. Add (método)

Agregue las estadísticas en dos JET_THREADSTATS estructuras.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function Add ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Add(t1, t2)
```

``` csharp
public static JET_THREADSTATS Add(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a>Parámetros

  - t1  
    Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Primer JET_THREADSTATS.

<!-- end list -->

  - T2  
    Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Segundo JET_THREADSTATS.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
JET_THREADSTATS que contiene el resultado de agregar las estadísticas en T1 y T2.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Estructura de JET_THREADSTATS](./jet-threadstats-structure2.md)

[Miembros de JET_THREADSTATS](./jet-threadstats-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
