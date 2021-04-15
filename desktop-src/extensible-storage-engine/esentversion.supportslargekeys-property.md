---
description: 'Más información sobre: EsentVersion. SupportsLargeKeys (propiedad)'
title: Propiedad EsentVersion. SupportsLargeKeys
TOCTitle: 'SupportsLargeKeys property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversion.supportslargekeys(v=EXCHG.10)
ms:contentKeyID: 55103180
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
- Microsoft.Isam.Esent.Interop.EsentVersion.get_SupportsLargeKeys
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43ee88b7c0e190d9c717c087deeb5fc4556e6575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649311"
---
# <a name="esentversionsupportslargekeys-property"></a>Propiedad EsentVersion. SupportsLargeKeys

Obtiene un valor que indica si \> se admiten claves grandes (255 bytes). El tamaño de la clave de un índice se puede especificar en el objeto [JET_INDEXCREATE](./jet-indexcreate-class.md) .

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared ReadOnly Property SupportsLargeKeys As Boolean
    Get
'Usage
Dim value As Boolean

value = EsentVersion.SupportsLargeKeys
```

``` csharp
public static bool SupportsLargeKeys { get; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase EsentVersion](./esentversion-class.md)

[Miembros de EsentVersion](./esentversion-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
