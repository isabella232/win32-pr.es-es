---
description: 'Más información acerca de: estructura de JET_COLUMNID'
title: Estructura de JET_COLUMNID
TOCTitle: JET_COLUMNID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_COLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid(v=EXCHG.10)
ms:contentKeyID: 39510915
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 163c10250e9d1f109b9557f8d222790c71561f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678379"
---
# <a name="jet_columnid-structure"></a>Estructura de JET_COLUMNID

Un JET_COLUMNID identifica una columna dentro de una tabla.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Structure JET_COLUMNID _
    Implements IEquatable(Of JET_COLUMNID), IComparable(Of JET_COLUMNID),  _
    IFormattable
'Usage
Dim instance As JET_COLUMNID
```

``` csharp
public struct JET_COLUMNID : IEquatable<JET_COLUMNID>, 
    IComparable<JET_COLUMNID>, IFormattable
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de JET_COLUMNID](./jet-columnid-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
