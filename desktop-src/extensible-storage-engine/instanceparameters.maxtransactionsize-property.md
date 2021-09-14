---
description: 'Más información sobre: Propiedad InstanceParameters.MaxTransactionSize'
title: Propiedad InstanceParameters.MaxTransactionSize
TOCTitle: 'MaxTransactionSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtransactionsize(v=EXCHG.10)
ms:contentKeyID: 55103317
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTransactionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTransactionSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370d05364142a6fca7d84265dc8d29c7ab5c808
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964363"
---
# <a name="instanceparametersmaxtransactionsize-property"></a>Propiedad InstanceParameters.MaxTransactionSize

Obtiene o establece el porcentaje de almacén de versiones que puede usar la transacción más antigua antes de [VersionStoreOutOfMemory](./jet-err-enumeration.md) (valor predeterminado = 100).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property MaxTransactionSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTransactionSize

instance.MaxTransactionSize = value
```

``` csharp
public int MaxTransactionSize { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
