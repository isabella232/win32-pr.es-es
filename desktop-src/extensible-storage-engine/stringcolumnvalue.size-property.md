---
description: 'Más información sobre: StringColumnValue. Size (propiedad)'
title: StringColumnValue. Size (propiedad)
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55104025
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.StringColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fdd9613061e049d45c4b9bce2772ff580ea1a0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716743"
---
# <a name="stringcolumnvaluesize-property"></a>StringColumnValue. Size (propiedad)

Obtiene el tamaño del valor de la columna. Esto devuelve 0 para las columnas de tamaño variable (es decir, binary y String).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase StringColumnValue](./stringcolumnvalue-class.md)

[Miembros de StringColumnValue](./stringcolumnvalue-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
