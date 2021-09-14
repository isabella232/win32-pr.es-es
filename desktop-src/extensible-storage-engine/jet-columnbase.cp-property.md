---
description: 'Más información sobre: JET_COLUMNBASE.cp'
title: JET_COLUMNBASE.cp, propiedad
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.cp(v=EXCHG.10)
ms:contentKeyID: 55103468
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8928ba3ae46283f856359b36d8f7c4c12f5891b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072530"
---
# <a name="jet_columnbasecp-property"></a>JET_COLUMNBASE.cp, propiedad

Obtiene la página de códigos de la columna. Esto solo es significativo para las columnas de tipo [Text](./jet-coltyp-enumeration.md) y [LongText](./jet-coltyp-enumeration.md).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As JET_CP

value = instance.cp
```

``` csharp
public JET_CP cp { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_COLUMNBASE clase](./jet-columnbase-class.md)

[JET_COLUMNBASE miembros](./jet-columnbase-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
