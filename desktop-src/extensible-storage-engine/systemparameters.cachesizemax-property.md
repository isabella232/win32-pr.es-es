---
description: 'Más información sobre: SystemParameters. CacheSizeMax (propiedad)'
title: Propiedad SystemParameters. CacheSizeMax
TOCTitle: 'CacheSizeMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesizemax(v=EXCHG.10)
ms:contentKeyID: 55104037
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7b03df288a0263cf6b79281f5ed79330dfd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278933"
---
# <a name="systemparameterscachesizemax-property"></a>Propiedad SystemParameters. CacheSizeMax

Obtiene o establece el tamaño máximo de la memoria caché de páginas de base de datos. El tamaño está en páginas de base de datos. Si este parámetro se deja en su valor predeterminado, el tamaño máximo de la memoria caché se establecerá en el tamaño de la memoria física cuando se llame a JetInit.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Property CacheSizeMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSizeMax

SystemParameters.CacheSizeMax = value
```

``` csharp
public static int CacheSizeMax { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[SystemParameters (clase)](./systemparameters-class.md)

[Miembros de SystemParameters](./systemparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
