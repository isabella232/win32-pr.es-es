---
description: 'Más información sobre: JET_RETINFO.columnidNextTagged'
title: JET_RETINFO.columnidNextTagged, propiedad
TOCTitle: 'columnidNextTagged property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.columnidnexttagged(v=EXCHG.10)
ms:contentKeyID: 55103802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_columnidNextTagged
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f6e00dd4d5013d2d03bc2ebbcf6791ab532879dc4ef04f358a2b8c01a5130a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117893180"
---
# <a name="jet_retinfocolumnidnexttagged-property"></a>JET_RETINFO.columnidNextTagged, propiedad

Obtiene el columnid de la columna etiquetada, multivalor o dispersa recuperada cuando se recuperan todas las columnas etiquetadas pasando 0 como columnid a JetRetrieveColumn.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidNextTagged As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_RETINFO
Dim value As JET_COLUMNID

value = instance.columnidNextTagged
```

``` csharp
public JET_COLUMNID columnidNextTagged { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_RETINFO clase](./jet-retinfo-class.md)

[JET_RETINFO miembros](./jet-retinfo-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
