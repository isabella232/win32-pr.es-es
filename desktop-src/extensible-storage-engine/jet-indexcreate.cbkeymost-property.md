---
description: 'Más información sobre: JET_INDEXCREATE.cbKeyMost'
title: JET_INDEXCREATE.cbKeyMost, propiedad
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
ms.openlocfilehash: 17908b19cba3ed047b98f4532982001019516d9b32e2799c29a6671cbd862fe7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232685"
---
# <a name="jet_indexcreatecbkeymost-property"></a>JET_INDEXCREATE.cbKeyMost, propiedad

Obtiene o establece el tamaño máximo permitido, en bytes, para las claves del índice. El tamaño máximo de clave mínimo admitido es JET_cbKeyMostMin (255), que es el tamaño de clave máximo heredado. El tamaño máximo de clave depende del tamaño de página de la base de [datos DatabasePageSize.](./jet-param-enumeration.md) El tamaño máximo de clave se puede recuperar con [KeyMost.](./systemparameters.keymost-property.md) Este parámetro se omite en Windows XP y Windows Server 2003. A diferencia de la API no administrada, **IndexKeyMost()** (JET_bitIndexKeyMost) no es necesario, se agregará automáticamente.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INDEXCREATE clase](./jet-indexcreate-class.md)

[JET_INDEXCREATE miembros](./jet-indexcreate-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
