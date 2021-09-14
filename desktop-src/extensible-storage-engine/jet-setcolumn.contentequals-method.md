---
description: 'Más información sobre: JET_SETCOLUMN. Método ContentEquals'
title: JET_SETCOLUMN. Método ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ContentEquals(Microsoft.Isam.Esent.Interop.JET_SETCOLUMN)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 489d42a72033ba942a359d8f3244b154dae9e3c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248774"
---
# <a name="jet_setcolumncontentequals-method"></a>JET_SETCOLUMN. Método ContentEquals

Devuelve un valor que indica si esta instancia es igual a otra instancia.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_SETCOLUMN _
) As Boolean
'Usage
Dim instance As JET_SETCOLUMN
Dim other As JET_SETCOLUMN
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_SETCOLUMN other
)
```

#### <a name="parameters"></a>Parámetros

  - otro  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SETCOLUMN](./jet-setcolumn-class.md)  
    
    Instancia de que se va a comparar con esta instancia.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

#### <a name="implements"></a>Implementaciones

[IContentEquatable \<T\> . ContentEquals(T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_SETCOLUMN clase](./jet-setcolumn-class.md)

[JET_SETCOLUMN miembros](./jet-setcolumn-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
