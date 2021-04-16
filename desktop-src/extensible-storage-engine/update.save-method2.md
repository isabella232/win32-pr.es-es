---
description: 'Más información sobre: método Update. Save'
title: Update. Save (método)
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
ms.openlocfilehash: 57693d3952f011127e60fdfb70dd2352c2f15207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542419"
---
# <a name="updatesave-method"></a>Update. Save (método)

Actualice el ID. de la.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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

## <a name="remarks"></a>Observaciones

Guardar es el último paso para realizar una inserción o una actualización. La actualización se inicia llamando a crear un objeto Update y llamando a JetSetColumn o JetSetColumns una o varias veces para establecer el estado del registro. Por último, se llama a Update para completar la operación de actualización. Los índices solo se actualizan mediante Update o y no durante JetSetColumn ni JetSetColumns.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Update (clase)](./update-class.md)

[Actualizar miembros](./update-members.md)

[Guardar sobrecarga](./update.save-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
