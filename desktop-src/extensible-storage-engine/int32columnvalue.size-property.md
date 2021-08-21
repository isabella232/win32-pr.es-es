---
description: Más información sobre la propiedad Int32ColumnValue.Size
title: Int32ColumnValue.Size, propiedad
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int32columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55103332
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.get_Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 648f6b7250f31983d1a03db4e0fffceb2a5e9aaa7806c030b17fae75b755e44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118767785"
---
# <a name="int32columnvaluesize-property"></a>Int32ColumnValue.Size, propiedad

Obtiene el tamaño del valor de la columna. Esto devuelve 0 para las columnas de tamaño variable (es decir, binario y cadena).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

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

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Int32ColumnValue (clase)](./int32columnvalue-class.md)

[Miembros Int32ColumnValue](./int32columnvalue-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
