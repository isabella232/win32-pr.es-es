---
description: 'Más información sobre: InstanceParameters. MaxTransactionSize (propiedad)'
title: Propiedad InstanceParameters. MaxTransactionSize
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910502"
---
# <a name="instanceparametersmaxtransactionsize-property"></a>Propiedad InstanceParameters. MaxTransactionSize

Obtiene o establece el porcentaje del almacén de versiones que la transacción más antigua puede usar antes de [VersionStoreOutOfMemory](./jet-err-enumeration.md) (valor predeterminado = 100).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros de InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
