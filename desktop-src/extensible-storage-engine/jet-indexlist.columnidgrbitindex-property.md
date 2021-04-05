---
description: 'Más información acerca de: propiedad JET_INDEXLIST. columnidgrbitIndex'
title: Propiedad JET_INDEXLIST. columnidgrbitIndex
TOCTitle: 'columnidgrbitIndex property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidgrbitindex(v=EXCHG.10)
ms:contentKeyID: 55103615
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidgrbitIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae8d31661451a2bd1c7c5f942141c27ae552c578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911762"
---
# <a name="jet_indexlistcolumnidgrbitindex-property"></a>Propiedad JET_INDEXLIST. columnidgrbitIndex

Obtiene el columnid de la columna de la tabla temporal que almacena el grbits que se usa en el índice. Vea [CreateIndexGrbit](./createindexgrbit-enumeration.md). La columna es de tipo [Long](./jet-coltyp-enumeration.md).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property columnidgrbitIndex As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbitIndex
```

``` csharp
public JET_COLUMNID columnidgrbitIndex { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INDEXLIST (clase)](./jet-indexlist-class.md)

[Miembros de JET_INDEXLIST](./jet-indexlist-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
