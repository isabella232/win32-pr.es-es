---
description: Más información sobre el método Update.Save
title: Método Update.Save
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75927144f887ab5cd7dbfe05c6d8fbf4c690a0e29786c1834fa00f8e29fae76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890066"
---
# <a name="updatesave-method"></a>Método Update.Save

Actualice el tableid.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a>Comentarios

Guardar es el último paso para realizar una inserción o una actualización. La actualización se inicia mediante una llamada a la creación de un objeto Update y, a continuación, llamando a JetSetColumn o JetSetColumns una o varias veces para establecer el estado del registro. Por último, se llama a Update para completar la operación de actualización. Los índices solo se actualizan mediante Update o y no durante JetSetColumn o JetSetColumns.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Actualizar clase](./update-class.md)

[Actualizar miembros](./update-members.md)

[Guardar sobrecarga](./update.save-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
