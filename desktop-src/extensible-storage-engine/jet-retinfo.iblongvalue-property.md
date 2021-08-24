---
description: 'Más información sobre: JET_RETINFO.ibLongValue'
title: JET_RETINFO.ibLongValue, propiedad
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103801
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 755a22e4cb0dbbee9d10ee45224ca54007a782f89f6220489722881dfe8524e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107309"
---
# <a name="jet_retinfoiblongvalue-property"></a>JET_RETINFO.ibLongValue, propiedad

Obtiene o establece el desplazamiento en el primer byte que se va a recuperar de una columna de tipo [LongBinary](./jet-coltyp-enumeration.md)o [LongText](./jet-coltyp-enumeration.md).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_RETINFO clase](./jet-retinfo-class.md)

[JET_RETINFO miembros](./jet-retinfo-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
