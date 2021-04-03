---
description: 'Más información sobre: ColumnStream. Write (método)'
title: ColumnStream. Write (método)
TOCTitle: 'Write method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Write(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.write(v=EXCHG.10)
ms:contentKeyID: 55100987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77b62e7dd028da3452082c973690ce0c0210b438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083290"
---
# <a name="columnstreamwrite-method"></a>ColumnStream. Write (método)

Escribe una secuencia de bytes en la secuencia actual y avanza la posición actual en esta secuencia según el número de bytes escritos.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Overrides Sub Write ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
)
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer

instance.Write(buffer, offset, count)
```

``` csharp
public override void Write(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>Parámetros

  - buffer  
    Automáticamente \[\]  
    
    Búfer del que se va a escribir.

<!-- end list -->

  - offset  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Desplazamiento en el búfer que se va a escribir.

<!-- end list -->

  - count  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número de bytes que se van a escribir.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase ColumnStream](./columnstream-class.md)

[Miembros de ColumnStream](./columnstream-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
