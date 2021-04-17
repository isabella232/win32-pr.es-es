---
description: 'Más información sobre: StringColumnValue. Value (propiedad)'
title: StringColumnValue. Value (propiedad)
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55104098
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b1f5dc65f41e1714858c75bed2c22e23680b60cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697712"
---
# <a name="stringcolumnvaluevalue-property"></a>StringColumnValue. Value (propiedad)

Obtiene o establece el valor de la columna. Use [SetColumns (JET_SESID, JET_TABLEID \[ \] )](./api.setcolumns-method.md) para actualizar un registro con el valor de la columna.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property Value As String
    Get
    Set
'Usage
Dim instance As StringColumnValue
Dim value As String

value = instance.Value

instance.Value = value
```

``` csharp
public string Value { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase StringColumnValue](./stringcolumnvalue-class.md)

[Miembros de StringColumnValue](./stringcolumnvalue-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
