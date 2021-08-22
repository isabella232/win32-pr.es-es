---
description: 'Más información sobre: Método Update.Save (Byte , Int32, Int32)'
title: Método Update.Save (Byte , Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e586177075a34f3832486a9ace4a919abaad65dad21c0e54eba47b79f207be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603545"
---
# <a name="updatesave-method-byte--int32-int32"></a>Método Update.Save (Byte , Int32, Int32)

Actualice el tableid.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>Parámetros

  - marcador  
    Tipo: \[\]  
    
    Devuelve el marcador del registro actualizado. Puede ser NULL.

<!-- end list -->

  - bookmarkSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño del búfer de marcador.

<!-- end list -->

  - actualBookmarkSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Devuelve el tamaño real del marcador.

## <a name="remarks"></a>Comentarios

Guardar es el último paso para realizar una inserción o una actualización. La actualización se inicia mediante una llamada a la creación de un objeto Update y, a continuación, llamando a JetSetColumn o JetSetColumns una o varias veces para establecer el estado del registro. Por último, se llama a Update para completar la operación de actualización. Los índices solo se actualizan mediante Update o y no durante JetSetColumn o JetSetColumns.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Actualizar clase](./update-class.md)

[Actualizar miembros](./update-members.md)

[Guardar sobrecarga](./update.save-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
