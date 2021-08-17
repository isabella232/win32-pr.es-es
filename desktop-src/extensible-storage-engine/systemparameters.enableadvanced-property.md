---
description: 'Más información sobre: Propiedad SystemParameters.EnableAdvanced'
title: Propiedad SystemParameters.EnableAdvanced
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07fd683ad6f2f0d2a9afd88b46a7786131e15c370c9046945ad3e9594a533391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107008"
---
# <a name="systemparametersenableadvanced-property"></a>Propiedad SystemParameters.EnableAdvanced

Obtiene o establece un valor que indica si el motor de base de datos acepta o rechaza los cambios en un subconjunto de los parámetros del sistema. Este parámetro se usa junto con [Configuration](./systemparameters.configuration-property.md) para evitar que algunos parámetros del sistema se establezcan fuera de los valores predeterminados de la configuración seleccionada. Compatible con Windows Vista y versiones 2. Se omite en Windows XP y Windows Server 2003.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[SystemParameters (clase)](./systemparameters-class.md)

[Miembros SystemParameters](./systemparameters-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
