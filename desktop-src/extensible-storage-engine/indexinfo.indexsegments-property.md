---
description: 'Más información sobre: IndexInfo. IndexSegments (propiedad)'
title: Propiedad IndexInfo. IndexSegments
TOCTitle: 'IndexSegments property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.indexsegments(v=EXCHG.10)
ms:contentKeyID: 55103239
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
- Microsoft.Isam.Esent.Interop.IndexInfo.get_IndexSegments
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d366d3ddd5ba7a33faeb44459830dbaadcc221e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811162"
---
# <a name="indexinfoindexsegments-property"></a>Propiedad IndexInfo. IndexSegments

Obtiene los segmentos del índice.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public ReadOnly Property IndexSegments As IList(Of IndexSegment)
    Get
'Usage
Dim instance As IndexInfo
Dim value As IList(Of IndexSegment)

value = instance.IndexSegments
```

``` csharp
public IList<IndexSegment> IndexSegments { get; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Collections. Generic. IList](/dotnet/api/system.collections.generic.ilist-1)\<[IndexSegment](./indexsegment-class.md)\>  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase IndexInfo](./indexinfo-class.md)

[Miembros de IndexInfo](./indexinfo-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
