---
description: 'Más información acerca de: JET_LS. Equals (método, Object)'
title: JET_LS. Equals (método, Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.equals(v=EXCHG.10)
ms:contentKeyID: 39511834
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 033936eb1f8d5176eed1b052ba5ee5332c8c5a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277872"
---
# <a name="jet_lsequals-method-object"></a>JET_LS. Equals (método, Object)

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
Dim instance As JET_LS
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

[Estructura de JET_LS](./jet-ls-structure.md)

[Miembros de JET_LS](./jet-ls-members.md)

[Equals (sobrecarga)](./jet-ls.equals-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
