---
description: 'Más información sobre: ColumnStream. Read (método)'
title: ColumnStream. Read (método)
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678339"
---
# <a name="columnstreamread-method"></a>ColumnStream. Read (método)

Lee una secuencia de bytes en el flujo actual y avanza la posición en el flujo según el número de bytes leídos.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>Parámetros

  - buffer  
    Automáticamente \[\]  
    
    Búfer en el que se va a leer.

<!-- end list -->

  - offset  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Desplazamiento en el búfer en el que se va a leer.

<!-- end list -->

  - count  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número de bytes que se va a leer.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Int32](/dotnet/api/system.int32)  
Número de bytes leídos en el búfer.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase ColumnStream](./columnstream-class.md)

[Miembros de ColumnStream](./columnstream-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
