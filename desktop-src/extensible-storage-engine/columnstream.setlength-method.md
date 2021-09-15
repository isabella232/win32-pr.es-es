---
description: 'Más información sobre: Método ColumnStream.SetLength'
title: Método ColumnStream.SetLength
TOCTitle: 'SetLength method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.SetLength(System.Int64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.setlength(v=EXCHG.10)
ms:contentKeyID: 55100986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.SetLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.SetLength
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fccf32d6494427811c3db8a2d2f4b71a2909a733
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465737"
---
# <a name="columnstreamsetlength-method"></a>Método ColumnStream.SetLength

Establece la longitud del flujo.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Overrides Sub SetLength ( _
    value As Long _
)
'Usage
Dim instance As ColumnStream
Dim value As Long

instance.SetLength(value)
```

``` csharp
public override void SetLength(
    long value
)
```

#### <a name="parameters"></a>Parámetros

  - value  
    Tipo: [System.Int64](/dotnet/api/system.int64)  
    
    Longitud deseada, en bytes.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[ColumnStream (clase)](./columnstream-class.md)

[Miembros columnStream](./columnstream-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
