---
description: 'Más información sobre: JET_RSTINFO. Método ContentEquals'
title: JET_RSTINFO. Método ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_RSTINFO.ContentEquals(Microsoft.Isam.Esent.Interop.JET_RSTINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103884
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c724368619a619c3fe337b90661b60ccc2c5c26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965595"
---
# <a name="jet_rstinfocontentequals-method"></a>JET_RSTINFO. Método ContentEquals

Devuelve un valor que indica si esta instancia es igual a otra instancia.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_RSTINFO _
) As Boolean
'Usage
Dim instance As JET_RSTINFO
Dim other As JET_RSTINFO
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_RSTINFO other
)
```

#### <a name="parameters"></a>Parámetros

  - otro  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)  
    
    Instancia de que se va a comparar con esta instancia.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si las dos instancias son iguales.  

#### <a name="implements"></a>Implementaciones

[IContentEquatable \<T\> . ContentEquals(T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_RSTINFO clase](./jet-rstinfo-class.md)

[JET_RSTINFO miembros](./jet-rstinfo-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
