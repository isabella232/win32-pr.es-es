---
description: 'Más información sobre: método Update. SaveAndGotoBookmark'
title: Método Update. SaveAndGotoBookmark
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d682657b9821f782af339a3d0c3253b6fa771d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715289"
---
# <a name="updatesaveandgotobookmark-method"></a>Método Update. SaveAndGotoBookmark

Actualice el TABLEID y coloque el TABLEID en el registro que se modificó. Esto puede ser útil al insertar un registro porque, de forma predeterminada, el TABLEID permanece en su ubicación anterior.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a>Observaciones

Guardar es el último paso para realizar una inserción o una actualización. La actualización se inicia llamando a crear un objeto Update y llamando a JetSetColumn o JetSetColumns una o varias veces para establecer el estado del registro. Por último, se llama a Update para completar la operación de actualización. Los índices solo se actualizan mediante Update o y no durante JetSetColumn ni JetSetColumns.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Update (clase)](./update-class.md)

[Actualizar miembros](./update-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
