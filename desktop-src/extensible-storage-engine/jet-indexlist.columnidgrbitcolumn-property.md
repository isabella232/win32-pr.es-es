---
description: 'Más información acerca de: propiedad JET_INDEXLIST. columnidgrbitColumn'
title: Propiedad JET_INDEXLIST. columnidgrbitColumn
TOCTitle: 'columnidgrbitColumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidgrbitcolumn(v=EXCHG.10)
ms:contentKeyID: 55103665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidgrbitColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidgrbitColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18be8455f2618265d77991b7c839f21ff04ef497
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716685"
---
# <a name="jet_indexlistcolumnidgrbitcolumn-property"></a>Propiedad JET_INDEXLIST. columnidgrbitColumn

Obtiene el columnid de la columna de la tabla temporal que almacena el grbit que se aplica a la columna indizada. Vea [IndexKeyGrbit](./indexkeygrbit-enumeration.md). La columna es de tipo [Long](./jet-coltyp-enumeration.md).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property columnidgrbitColumn As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbitColumn
```

``` csharp
public JET_COLUMNID columnidgrbitColumn { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INDEXLIST (clase)](./jet-indexlist-class.md)

[Miembros de JET_INDEXLIST](./jet-indexlist-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
