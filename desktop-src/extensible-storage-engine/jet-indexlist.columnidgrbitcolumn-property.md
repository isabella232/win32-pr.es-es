---
description: 'Más información sobre: JET_INDEXLIST.columnidgrbitColumn'
title: JET_INDEXLIST.columnidgrbitColumn, propiedad
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
ms.openlocfilehash: 8588b5e7647507eb417610baab685e27e9c00a836f56ed6f1da499b0b66121e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038963"
---
# <a name="jet_indexlistcolumnidgrbitcolumn-property"></a>JET_INDEXLIST.columnidgrbitColumn, propiedad

Obtiene el columnid de la columna de la tabla temporal que almacena el grbit que se aplica a la columna indizada. Vea [IndexKeyGrbit](./indexkeygrbit-enumeration.md). La columna es de tipo [Long.](./jet-coltyp-enumeration.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

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

Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INDEXLIST clase](./jet-indexlist-class.md)

[JET_INDEXLIST miembros](./jet-indexlist-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
