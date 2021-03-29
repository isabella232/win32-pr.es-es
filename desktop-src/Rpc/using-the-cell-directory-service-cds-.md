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
# <a name="using-the-cell-directory-service-cds"></a><span data-ttu-id="8b6c0-104">Uso del Servicio de directorio de celdas (CDS)</span><span class="sxs-lookup"><span data-stu-id="8b6c0-104">Using the Cell Directory Service (CDS)</span></span>

<span data-ttu-id="8b6c0-105">Si tiene CDS, puede usarlo en lugar del localizador de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-105">If you have CDS, you can use it instead of Microsoft Locator.</span></span> <span data-ttu-id="8b6c0-106">Cambie las entradas del registro como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="8b6c0-106">Change the registry entries as shown:</span></span>

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

<span data-ttu-id="8b6c0-107">Al cambiar estas entradas, se señalará a un equipo de puerta de enlace que ejecuta NSID.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-107">Changing these entries will point to a gateway computer that is running the NSID.</span></span> <span data-ttu-id="8b6c0-108">Se usará como localizador maestro.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-108">This will be used as the master locator.</span></span> <span data-ttu-id="8b6c0-109">En caso de que se produzca un bloqueo, no habrá ninguna búsqueda de un reemplazo.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-109">In the event of a crash, there will be no search for a replacement.</span></span>

 

 




