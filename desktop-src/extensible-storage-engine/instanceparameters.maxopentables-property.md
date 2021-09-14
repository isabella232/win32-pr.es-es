---
description: 'Más información sobre: Propiedad InstanceParameters.MaxOpenTables'
title: Propiedad InstanceParameters.MaxOpenTables
TOCTitle: 'MaxOpenTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxopentables(v=EXCHG.10)
ms:contentKeyID: 55107442
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 623d2f1fe536fb2b5916c96e97de8904fa5a7c86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963019"
---
# <a name="instanceparametersmaxopentables-property"></a>Propiedad InstanceParameters.MaxOpenTables

Obtiene o establece el número de recursos de árbol B+ reservados para esta instancia.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property MaxOpenTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxOpenTables

instance.MaxOpenTables = value
```

``` csharp
public int MaxOpenTables { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
