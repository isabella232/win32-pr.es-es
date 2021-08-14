---
description: 'Más información sobre: Propiedad StringColumnValue.Value'
title: Propiedad StringColumnValue.Value
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
ms.openlocfilehash: cfc3167cc62faa2b7c25a670bc8ad1bc7cc31795a62361e36025c09f53ffbac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485387"
---
# <a name="stringcolumnvaluevalue-property"></a>Propiedad StringColumnValue.Value

Obtiene o establece el valor de la columna. Use [SetColumns(JET_SESID, JET_TABLEID, \[ \] ) para](./api.setcolumns-method.md) actualizar un registro con el valor de columna.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

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

Tipo: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[StringColumnValue (clase)](./stringcolumnvalue-class.md)

[Miembros StringColumnValue](./stringcolumnvalue-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
