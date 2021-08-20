---
title: Uso del Servicio de directorio de celdas (CDS)
description: Si tiene CDS, puede usarlo en lugar de Microsoft Locator.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- Llamada a procedimiento remoto RPC , tareas, mediante el servicio de directorio de celdas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df9058d917396a4e2e2dc3579768c3f3d5b46242b34c0fa5411c6d2204ed20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010643"
---
# <a name="using-the-cell-directory-service-cds"></a>Uso del Servicio de directorio de celdas (CDS)

Si tiene CDS, puede usarlo en lugar de Microsoft Locator. Cambie las entradas del Registro como se muestra a continuación:

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

El cambio de estas entradas apuntará a un equipo de puerta de enlace que ejecuta el NSID. Se usará como localizador maestro. En caso de bloqueo, no habrá ninguna búsqueda de reemplazo.

 

 




