---
description: 'Más información acerca de: JET_COLUMNDEF. Método ContentEquals'
title: JET_COLUMNDEF. Método ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNDEF)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103479
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f4527edef1fd8567ec3f4973dddc67548e79946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155028"
---
# <a name="jet_columndefcontentequals-method"></a>JET_COLUMNDEF. Método ContentEquals

Devuelve un valor que indica si esta instancia es igual a otra instancia de.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNDEF _
) As Boolean
'Usage
Dim instance As JET_COLUMNDEF
Dim other As JET_COLUMNDEF
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNDEF other
)
```

#### <a name="parameters"></a>Parámetros

  - Otros  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)  
    
    Instancia de que se va a comparar con esta instancia.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

#### <a name="implements"></a>Implementaciones

[IContentEquatable \<T\> . ContentEquals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_COLUMNDEF (clase)](./jet-columndef-class.md)

[Miembros de JET_COLUMNDEF](./jet-columndef-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
