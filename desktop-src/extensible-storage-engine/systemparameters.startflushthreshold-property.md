---
description: 'Más información sobre: Propiedad SystemParameters.StartFlushThreshold'
title: Propiedad SystemParameters.StartFlushThreshold
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49a868bf06f6994d61e3f901d5d9a447d2ef63c7909c33db3689fda343e16c27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484864"
---
# <a name="systemparametersstartflushthreshold-property"></a>Propiedad SystemParameters.StartFlushThreshold

Obtiene o establece el umbral en el que la caché de páginas de la base de datos comienza a expulsar páginas de la memoria caché para hacer espacio para las páginas que no están almacenadas en caché. Cuando el número de búferes de página de la memoria caché cae por debajo de este umbral, se inicia un proceso en segundo plano para reponer ese grupo de búferes disponibles. Este umbral siempre es relativo al tamaño máximo de caché establecido por JET_paramCacheSizeMax. Este umbral también debe ser siempre menor que el umbral de detección establecido por JET_paramStopFlushThreshold. El alto de distancia del umbral de inicio determinará el tiempo de respuesta que debe tener la caché de páginas de la base de datos para generar búferes disponibles antes de que la aplicación los necesite. Un umbral de inicio alto dará al proceso en segundo plano más tiempo para reaccionar. Sin embargo, un umbral de inicio alto implica un umbral de detección más alto y eso reducirá el tamaño efectivo de la caché de páginas de la base de datos.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[SystemParameters (clase)](./systemparameters-class.md)

[Miembros SystemParameters](./systemparameters-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
