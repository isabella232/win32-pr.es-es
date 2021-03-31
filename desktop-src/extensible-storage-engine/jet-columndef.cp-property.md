---
description: 'Más información acerca de: JET_COLUMNDEF. CP (propiedad)'
title: JET_COLUMNDEF. CP (propiedad)
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cp(v=EXCHG.10)
ms:contentKeyID: 55103411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df383b212105a4b871f0c44d341d6113abf94d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155396"
---
# <a name="jet_columndefcp-property"></a>JET_COLUMNDEF. CP (propiedad)

Obtiene o establece la página de códigos de la columna. Esto solo es significativo para las columnas de tipo [Text](./jet-coltyp-enumeration.md) y [LongText](./jet-coltyp-enumeration.md).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.ISAM.esent.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_COLUMNDEF (clase)](./jet-columndef-class.md)

[Miembros de JET_COLUMNDEF](./jet-columndef-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
