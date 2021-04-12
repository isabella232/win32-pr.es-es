---
description: 'Más información acerca de: JET_INDEXRANGE. Método ContentEquals'
title: JET_INDEXRANGE. Método ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_INDEXRANGE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexrange.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8934ed14339c24348199fe50b09bbf2da3e94207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277889"
---
# <a name="jet_indexrangecontentequals-method"></a>JET_INDEXRANGE. Método ContentEquals

Devuelve un valor que indica si esta instancia es igual a otra instancia de.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_INDEXRANGE _
) As Boolean
'Usage
Dim instance As JET_INDEXRANGE
Dim other As JET_INDEXRANGE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_INDEXRANGE other
)
```

#### <a name="parameters"></a>Parámetros

  - Otros  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INDEXRANGE](./jet-indexrange-class.md)  
    
    Instancia de que se va a comparar con esta instancia.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

#### <a name="implements"></a>Implementaciones

[IContentEquatable \<T\> . ContentEquals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INDEXRANGE (clase)](./jet-indexrange-class.md)

[Miembros de JET_INDEXRANGE](./jet-indexrange-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
