---
description: 'Más información sobre: Método ColumnStream.Seek'
title: Método ColumnStream.Seek
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170350"
---
# <a name="columnstreamseek-method"></a>Método ColumnStream.Seek

Establece la posición en la secuencia actual.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a>Parámetros

  - offset  
    Tipo: [System.Int64](/dotnet/api/system.int64)  
    
    Desplazamiento de bytes con respecto al parámetro de origen.

<!-- end list -->

  - origen  
    Tipo: [System.IO.SeekOrigin](/dotnet/api/system.io.seekorigin)  
    
    SeekOrigin que indica el punto de referencia de la nueva posición.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Int64](/dotnet/api/system.int64)  
Nueva posición en la secuencia actual.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[ColumnStream (clase)](./columnstream-class.md)

[Miembros ColumnStream](./columnstream-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
