---
description: 'Más información sobre: InstanceParameters. EnableDbScanInRecovery (propiedad)'
title: Propiedad InstanceParameters. EnableDbScanInRecovery
TOCTitle: 'EnableDbScanInRecovery property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enabledbscaninrecovery(v=EXCHG.10)
ms:contentKeyID: 55107448
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableDbScanInRecovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableDbScanInRecovery
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c6d492b2c101305b3038c300c77467d14dc480e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912181"
---
# <a name="instanceparametersenabledbscaninrecovery-property"></a>Propiedad InstanceParameters. EnableDbScanInRecovery

Obtiene o establece un valor que indica si el mantenimiento de la base de datos se debe ejecutar durante la recuperación.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property EnableDbScanInRecovery As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.EnableDbScanInRecovery

instance.EnableDbScanInRecovery = value
```

``` csharp
public int EnableDbScanInRecovery { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros de InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
