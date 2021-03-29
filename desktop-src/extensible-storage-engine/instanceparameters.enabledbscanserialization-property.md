---
description: 'Más información sobre: InstanceParameters. EnableDBScanSerialization (propiedad)'
title: Propiedad InstanceParameters. EnableDBScanSerialization
TOCTitle: 'EnableDBScanSerialization property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enabledbscanserialization(v=EXCHG.10)
ms:contentKeyID: 55103555
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableDBScanSerialization
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableDBScanSerialization
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c514218b43d1f291abc01d384cdb47f339163cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360485"
---
# <a name="instanceparametersenabledbscanserialization-property"></a>Propiedad InstanceParameters. EnableDBScanSerialization

Obtiene o establece un valor que indica si está habilitada la serialización del mantenimiento de la base de datos para las bases de datos que comparten el mismo disco.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property EnableDBScanSerialization As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.EnableDBScanSerialization

instance.EnableDBScanSerialization = value
```

``` csharp
public bool EnableDBScanSerialization { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros de InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
