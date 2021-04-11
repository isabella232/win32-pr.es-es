---
description: 'Más información sobre: API. TryMoveNext (método)'
title: Método API. TryMoveNext
TOCTitle: 'TryMoveNext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveNext(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovenext(v=EXCHG.10)
ms:contentKeyID: 55100887
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b4b4e1f296e5549ba3823f698cdcb5cc9f9f42a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154032"
---
# <a name="apitrymovenext-method"></a>Método API. TryMoveNext

Intente moverse al siguiente registro de la tabla. Si no hay un registro siguiente, devuelve false, si se produce un error diferente, se produce una excepción.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function TryMoveNext ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveNext(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveNext(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se va a colocar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True si el movimiento se realizó correctamente.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
