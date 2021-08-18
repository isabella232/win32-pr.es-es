---
description: Más información sobre el campo VistaGrbits.IndexDisallowTruncation
title: Campo VistaGrbits.IndexDisallowTruncation (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: IndexDisallowTruncation field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexDisallowTruncation
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexdisallowtruncation(v=EXCHG.10)
ms:contentKeyID: 55104424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexDisallowTruncation
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexDisallowTruncation
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 130a109e8e368aabd6113acd683473dd9324c1cb8a0fa6d7af09c05e2a6301b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117889857"
---
# <a name="vistagrbitsindexdisallowtruncation-field"></a>Campo VistaGrbits.IndexDisallowTruncation

Si se especifica esta marca, se producirá un error en cualquier actualización del índice que provocaría un error en una clave truncada con [KeyTruncated](./jet-err-enumeration.md). De lo contrario, las claves se truncarán en modo silencioso.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Const IndexDisallowTruncation As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexDisallowTruncation
```

``` csharp
public const CreateIndexGrbit IndexDisallowTruncation
```

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[VistaGrbits (clase)](./vistagrbits-class.md)

[Miembros de VistaGrbits](./vistagrbits-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
