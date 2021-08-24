---
description: 'Más información sobre: Propiedad SystemParameters.HungIOThreshold'
title: Propiedad SystemParameters.HungIOThreshold
TOCTitle: 'HungIOThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.HungIOThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.hungiothreshold(v=EXCHG.10)
ms:contentKeyID: 55104041
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.HungIOThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_HungIOThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.HungIOThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_HungIOThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 587893371aabb6d47e4560c0a8d113ae8e337d5f395b00edbcf32268635d1238
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603590"
---
# <a name="systemparametershungiothreshold-property"></a>Propiedad SystemParameters.HungIOThreshold

Obtiene o establece el umbral para lo que se considera una E/S desahora sobre la que se debe actuar.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property HungIOThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.HungIOThreshold

SystemParameters.HungIOThreshold = value
```

``` csharp
public static int HungIOThreshold { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[SystemParameters (clase)](./systemparameters-class.md)

[Miembros SystemParameters](./systemparameters-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
