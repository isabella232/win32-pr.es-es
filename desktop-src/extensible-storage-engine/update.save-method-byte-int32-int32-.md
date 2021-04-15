---
description: 'Más información sobre: método Update. Save (byte, Int32, Int32)'
title: Método Update. Save (byte, Int32, Int32)
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
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497620"
---
# <a name="updatesave-method-byte--int32-int32"></a>Método Update. Save (byte, Int32, Int32)

Actualice el ID. de la.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Automáticamente \[\]  
    
    Devuelve el marcador del registro actualizado. Puede ser NULL.

<!-- end list -->

  - bookmarkSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Tamaño del búfer del marcador.

<!-- end list -->

  - actualBookmarkSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Devuelve el tamaño real del marcador.

## <a name="remarks"></a>Observaciones

Guardar es el último paso para realizar una inserción o una actualización. La actualización se inicia llamando a crear un objeto Update y llamando a JetSetColumn o JetSetColumns una o varias veces para establecer el estado del registro. Por último, se llama a Update para completar la operación de actualización. Los índices solo se actualizan mediante Update o y no durante JetSetColumn ni JetSetColumns.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Update (clase)](./update-class.md)

[Actualizar miembros](./update-members.md)

[Guardar sobrecarga](./update.save-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
