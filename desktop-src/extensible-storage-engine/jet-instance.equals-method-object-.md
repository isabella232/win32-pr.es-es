---
description: 'Más información sobre: JET_INSTANCE. Método Equals (Object)'
title: JET_INSTANCE. Método Equals (Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39515717
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b13393b487abb4de65360f5199ae1123d3f076e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887492"
---
# <a name="jet_instanceequals-method-object"></a>JET_INSTANCE. Método Equals (Object)

Devuelve un valor que indica si esta instancia es igual a otra instancia.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
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
    Tipo: [System.Object](/dotnet/api/system.object)  
    
    Objeto que se va a comparar con esta instancia.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_INSTANCE estructura](./jet-instance-structure.md)

[JET_INSTANCE miembros](./jet-instance-members.md)

[Sobrecarga igual a](./jet-instance.equals-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
