---
description: El \_32.dll Ws2 (y los protocolos en capas) llamará a WSPCleanup una vez para cada invocación de WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Limpieza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696399"
---
# <a name="cleanup"></a><span data-ttu-id="070ed-103">Limpieza</span><span class="sxs-lookup"><span data-stu-id="070ed-103">Cleanup</span></span>

<span data-ttu-id="070ed-104">El \_32.dll Ws2 (y los protocolos en capas) llamará a [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) una vez para cada invocación de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="070ed-104">The Ws2\_32.dll (and layered protocols) will call [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) once for each invocation of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span> <span data-ttu-id="070ed-105">En cada invocación, **WSPCleanup** debe disminuir un contador de referencia por proceso y, cuando el contador llega a cero, el proveedor de servicios debe prepararse para descargarse de la memoria.</span><span class="sxs-lookup"><span data-stu-id="070ed-105">On each invocation, **WSPCleanup** should decrement a per-process reference counter, and when the counter reaches zero, the service provider must prepare itself to be unloaded from memory.</span></span> <span data-ttu-id="070ed-106">El primer orden de negocio es finalizar la transmisión de los datos no enviados en los sockets configurados para un cierre estable.</span><span class="sxs-lookup"><span data-stu-id="070ed-106">The first order of business is to finish transmitting any unsent data on sockets that are configured for a graceful close.</span></span> <span data-ttu-id="070ed-107">A partir de ese momento, se liberarán todos los recursos retenidos por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="070ed-107">Thereafter, any and all resources held by the provider are to be freed.</span></span> <span data-ttu-id="070ed-108">El proveedor de servicios debe dejarse en un estado en el que se pueda reinicializar inmediatamente mediante una llamada a **WSPStartup**.</span><span class="sxs-lookup"><span data-stu-id="070ed-108">The service provider must be left in a state where it can be immediately reinitialized by a call to **WSPStartup**.</span></span>

 

 
