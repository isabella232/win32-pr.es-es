---
description: 'Más información sobre: InstanceParameters. TempDirectory (propiedad)'
title: Propiedad InstanceParameters. TempDirectory
TOCTitle: 'TempDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.tempdirectory(v=EXCHG.10)
ms:contentKeyID: 55103324
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_TempDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_TempDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bbe31b7f437f045f601b18daf92877784d58512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003085"
---
# <a name="instanceparameterstempdirectory-property"></a>Propiedad InstanceParameters. TempDirectory

Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá la base de datos temporal de la instancia.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property TempDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.TempDirectory

instance.TempDirectory = value
```

``` csharp
public string TempDirectory { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros de InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
