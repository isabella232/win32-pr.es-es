---
description: 'Más información acerca de: JET_ENUMCOLUMN. err (propiedad)'
title: JET_ENUMCOLUMN. err (propiedad)
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.err(v=EXCHG.10)
ms:contentKeyID: 55103499
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.err
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44bedfc0dcf6225c3d7084d4a4bfe07b0e059a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360138"
---
# <a name="jet_enumcolumnerr-property"></a>JET_ENUMCOLUMN. err (propiedad)

Obtiene el código de estado de la columna que es el resultado de la enumeración.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_ENUMCOLUMN (clase)](./jet-enumcolumn-class.md)

[Miembros de JET_ENUMCOLUMN](./jet-enumcolumn-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[ColumnSingleValue](./jet-wrn-enumeration.md)
