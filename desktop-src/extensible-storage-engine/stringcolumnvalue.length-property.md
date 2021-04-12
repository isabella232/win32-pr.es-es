---
description: 'Más información sobre: StringColumnValue. length (propiedad)'
title: StringColumnValue. length (propiedad)
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55104090
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Length
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7313f66bd25653a66ebd8567a21c0ad5431ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278040"
---
# <a name="stringcolumnvaluelength-property"></a>StringColumnValue. length (propiedad)

Obtiene la longitud de bytes de un valor de columna, que es cero si la columna es null; de lo contrario, coincide con la longitud de bytes del valor de cadena. La longitud de bytes se determina en suposición de dos bytes por carácter.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As StringColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase StringColumnValue](./stringcolumnvalue-class.md)

[Miembros de StringColumnValue](./stringcolumnvalue-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
