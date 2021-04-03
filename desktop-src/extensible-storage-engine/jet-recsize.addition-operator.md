---
description: 'Más información acerca de: JET_RECSIZE. Operador de suma'
title: JET_RECSIZE. Operador de suma (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_addition(v=EXCHG.10)
ms:contentKeyID: 39512451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c41fae92f6177bf0c39138ad33988a74c482e0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808521"
---
# <a name="jet_recsizeaddition-operator"></a>JET_RECSIZE. Operador de suma

Agregue los tamaños en dos estructuras de JET_RECSIZE.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Operator + ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left + right)
```

``` csharp
public static JET_RECSIZE operator +(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a>Parámetros

  - izquierda  
    Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Primer JET_RECSIZE.

<!-- end list -->

  - right  
    Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Segundo JET_RECSIZE.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)  
JET_RECSIZE que contiene el resultado de agregar los tamaños a la izquierda y a la derecha.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Estructura de JET_RECSIZE](./jet-recsize-structure2.md)

[Miembros de JET_RECSIZE](./jet-recsize-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
