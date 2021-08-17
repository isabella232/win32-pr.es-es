---
description: 'Más información sobre: JET_ENUMCOLUMN.cbData'
title: JET_ENUMCOLUMN.cbData, propiedad
TOCTitle: 'cbData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cbdata(v=EXCHG.10)
ms:contentKeyID: 55103617
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cbData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8a1674c4b4c47d6f6a1fa07b06806cd5202db95eb789e499485936ba438dcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766011"
---
# <a name="jet_enumcolumncbdata-property"></a>JET_ENUMCOLUMN.cbData, propiedad

Obtiene el tamaño del valor enumerado para la columna. Este miembro solo se usa si [err](./jet-enumcolumn.err-property.md) es igual a [ColumnSingleValue.](./jet-wrn-enumeration.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbData As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cbData
```

``` csharp
public int cbData { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_ENUMCOLUMN clase](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN miembros](./jet-enumcolumn-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
