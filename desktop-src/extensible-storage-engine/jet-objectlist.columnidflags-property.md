---
description: 'Más información sobre: JET_OBJECTLIST.columnidflags'
title: JET_OBJECTLIST.columnidflags, propiedad
TOCTitle: 'columnidflags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidflags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.columnidflags(v=EXCHG.10)
ms:contentKeyID: 55103772
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidflags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidflags
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_columnidflags
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_columnidflags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca7e2be41262578b2c4224ebcc97050b8e27bcec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126882905"
---
# <a name="jet_objectlistcolumnidflags-property"></a>JET_OBJECTLIST.columnidflags, propiedad

Obtiene el columnid de la columna de la tabla temporal que almacena las marcas de tabla (por ejemplo, la marca de tabla del sistema).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property columnidflags As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_OBJECTLIST
Dim value As JET_COLUMNID

value = instance.columnidflags
```

``` csharp
public JET_COLUMNID columnidflags { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_OBJECTLIST clase](./jet-objectlist-class.md)

[JET_OBJECTLIST miembros](./jet-objectlist-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
