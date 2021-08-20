---
description: Más información sobre el método IndexSegment.Equals (IndexSegment)
title: Método IndexSegment.Equals (IndexSegment)
TOCTitle: Equals method (IndexSegment)
ms:assetid: M:Microsoft.Isam.Esent.Interop.IndexSegment.Equals(Microsoft.Isam.Esent.Interop.IndexSegment)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexsegment.equals(v=EXCHG.10)
ms:contentKeyID: 55103276
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.IndexSegment.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 656fc4112f19f2152ea6d6eae3add2b5fef18445fbb4d920f9310ef47b8e48b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117896029"
---
# <a name="indexsegmentequals-method-indexsegment"></a>Método IndexSegment.Equals (IndexSegment)

Devuelve un valor que indica si esta instancia es igual a otra instancia.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Function Equals ( _
    other As IndexSegment _
) As Boolean
'Usage
Dim instance As IndexSegment
Dim other As IndexSegment
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    IndexSegment other
)
```

#### <a name="parameters"></a>Parámetros

  - Otros  
    Tipo: [Microsoft.Isam.Esent.Interop.IndexSegment](./indexsegment-class.md)  
    
    Instancia de que se va a comparar con esta instancia.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

#### <a name="implements"></a>Implementaciones

[IEquatable \<T\> . Equals(T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[IndexSegment (clase)](./indexsegment-class.md)

[Miembros indexSegment](./indexsegment-members.md)

[Sobrecarga igual a](./indexsegment.equals-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
