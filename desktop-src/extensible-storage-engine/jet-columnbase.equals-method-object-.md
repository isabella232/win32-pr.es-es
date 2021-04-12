---
description: 'Más información acerca de: JET_COLUMNBASE. Equals (método, Object)'
title: JET_COLUMNBASE. Equals (método, Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.equals(v=EXCHG.10)
ms:contentKeyID: 55103438
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63f5d17fcbd6f02c021c1604a2acab838de92b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279407"
---
# <a name="jet_columnbaseequals-method-object"></a>JET_COLUMNBASE. Equals (método, Object)

Devuelve un valor que indica si esta instancia es igual a otra instancia de.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_COLUMNBASE
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a>Parámetros

  - obj  
    Tipo: [System. Object](/dotnet/api/system.object)  
    
    Objeto que se va a comparar con esta instancia.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_COLUMNBASE (clase)](./jet-columnbase-class.md)

[Miembros de JET_COLUMNBASE](./jet-columnbase-members.md)

[Equals (sobrecarga)](./jet-columnbase.equals-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
