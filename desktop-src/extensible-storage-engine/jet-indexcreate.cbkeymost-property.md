---
description: 'Más información acerca de: propiedad JET_INDEXCREATE. cbKeyMost'
title: Propiedad JET_INDEXCREATE. cbKeyMost
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911465"
---
# <a name="jet_indexcreatecbkeymost-property"></a>Propiedad JET_INDEXCREATE. cbKeyMost

Obtiene o establece el tamaño máximo permitido, en bytes, para las claves del índice. El tamaño máximo de clave compatible mínimo es JET_cbKeyMostMin (255), que es el tamaño de clave máximo heredado. El tamaño máximo de la clave depende del tamaño de página de la base de datos [DatabasePageSize](./jet-param-enumeration.md). El tamaño máximo de la clave se puede recuperar con [KeyMost](./systemparameters.keymost-property.md). Este parámetro se omite en Windows XP y Windows Server 2003. A diferencia de la API no administrada, **IndexKeyMost ()** (JET_bitIndexKeyMost) no es necesario, sino que se agregará automáticamente.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INDEXCREATE (clase)](./jet-indexcreate-class.md)

[Miembros de JET_INDEXCREATE](./jet-indexcreate-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
