---
description: 'Más información sobre: JET_ENUMCOLUMNID.rgtagSequence'
title: JET_ENUMCOLUMNID.rgtagSequence, propiedad
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 026432a6d5b2363df09640141ec9f190d6637258692ce8233b32c004a1dbde86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765971"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a>JET_ENUMCOLUMNID.rgtagSequence, propiedad

Obtiene o establece la matriz de índices basados en uno en la matriz de valores de columna de una columna determinada. Un único elemento es una itagSequence que se define en JET_RETRIEVECOLUMN. Una itagSequence de 0 (cero) significa "skip". Una itagSequence de 1 significa devolver el primer valor de columna de la columna, 2 significa la segunda, y así sucesivamente.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: \[\]  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_ENUMCOLUMNID clase](./jet-enumcolumnid-class.md)

[JET_ENUMCOLUMNID miembros](./jet-enumcolumnid-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
