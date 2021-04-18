---
description: 'Más información sobre: ColumnValue. length (propiedad)'
title: ColumnValue. length (propiedad)
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c64e2b8e7b25be5b33d64591e16b982604e2fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707483"
---
# <a name="columnvaluelength-property"></a>ColumnValue. length (propiedad)

Obtiene la longitud de bytes de un valor de columna, que es cero si la columna es null; de lo contrario, coincide con el tamaño de las columnas de tamaño fijo y representa el valor real de longitud de bytes para las columnas de tamaño variable (es decir, binario y cadena). En el caso de las cadenas, la longitud se determina en dos bytes por carácter.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase ColumnValue](./columnvalue-class.md)

[Miembros de ColumnValue](./columnvalue-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
