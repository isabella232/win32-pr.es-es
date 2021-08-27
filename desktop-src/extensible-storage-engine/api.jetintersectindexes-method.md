---
description: Más información sobre el método Api.JetIntersectIndexes
title: Método Api.JetIntersectIndexes
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b2e9e259d9c90a3067931fbba425ab1b21e5c2a36a73563f593d3b280a40496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978037"
---
# <a name="apijetintersectindexes-method"></a>Método Api.JetIntersectIndexes

Calcula la intersección entre varios conjuntos de entradas de índice de distintos índices secundarios sobre la misma tabla. Esta operación es útil para buscar el conjunto de registros de una tabla que coinciden con dos o más criterios que se pueden expresar mediante intervalos de índice. Vea también [IntersectIndexes(JET_SESID, \[ \] ).](./api.intersectindexes-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - ranges  
    Tipo: \[\]  
    
    Un intervalo de índice que se va a formar una intersección. Los tableids de los intervalos deben tener intervalos de índice establecidos en ellos. Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) para crear un intervalo de índice.

<!-- end list -->

  - numRanges  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de intervalos de índice.

<!-- end list -->

  - recordlist  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)  
    
    Devuelve información sobre la tabla temporal que contiene los resultados de intersección.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)  
    
    Opciones de intersección.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
