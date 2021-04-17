---
description: 'Más información sobre: InstanceParameters. VersionStoreTaskQueueMax (propiedad)'
title: Propiedad InstanceParameters. VersionStoreTaskQueueMax
TOCTitle: 'VersionStoreTaskQueueMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.versionstoretaskqueuemax(v=EXCHG.10)
ms:contentKeyID: 55103554
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_VersionStoreTaskQueueMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd522fa46df40182b6dfe638e7663df8e9e56c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498154"
---
# <a name="instanceparametersversionstoretaskqueuemax-property"></a>Propiedad InstanceParameters. VersionStoreTaskQueueMax

Obtiene o establece el número de elementos de trabajo de limpieza en segundo plano que se pueden poner en cola en el grupo de subprocesos del motor de base de datos al mismo tiempo.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property VersionStoreTaskQueueMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.VersionStoreTaskQueueMax

instance.VersionStoreTaskQueueMax = value
```

``` csharp
public int VersionStoreTaskQueueMax { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros de InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
