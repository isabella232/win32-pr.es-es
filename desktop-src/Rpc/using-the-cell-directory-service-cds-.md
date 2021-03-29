---
title: Uso del Servicio de directorio de celdas (CDS)
description: Si tiene CDS, puede usarlo en lugar del localizador de Microsoft.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- RPC llamada a procedimiento remoto, tareas, uso del servicio de directorio de celdas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0029bf78308d6963d615daa04eaf87f3617ebbb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776117"
---
# <a name="using-the-cell-directory-service-cds"></a>Uso del Servicio de directorio de celdas (CDS)

Si tiene CDS, puede usarlo en lugar del localizador de Microsoft. Cambie las entradas del registro como se muestra a continuación:

``` syntax
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    NetworkAddress
 
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    Endpoint
```

Al cambiar estas entradas, se señalará a un equipo de puerta de enlace que ejecuta NSID. Se usará como localizador maestro. En caso de que se produzca un bloqueo, no habrá ninguna búsqueda de un reemplazo.

 

 




