---
description: 'Más información sobre: InstanceParameters. CreatePathIfNotExist (propiedad)'
title: Propiedad InstanceParameters. CreatePathIfNotExist
TOCTitle: 'CreatePathIfNotExist property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.createpathifnotexist(v=EXCHG.10)
ms:contentKeyID: 55103321
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d777c7bae3c375118488105e275edba59e57cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648249"
---
# <a name="instanceparameterscreatepathifnotexist-property"></a>Propiedad InstanceParameters. CreatePathIfNotExist

Obtiene o establece un valor que indica si ESENT creará silenciosamente carpetas que faltan en sus rutas de acceso del sistema de archivos.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property CreatePathIfNotExist As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CreatePathIfNotExist

instance.CreatePathIfNotExist = value
```

``` csharp
public bool CreatePathIfNotExist { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros de InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
