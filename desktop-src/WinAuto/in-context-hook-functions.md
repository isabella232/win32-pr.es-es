---
title: In-Context funciones de enlace
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Más información sobre: In-Context funciones de enlace'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279299"
---
# <a name="in-context-hook-functions"></a><span data-ttu-id="56471-103">In-Context funciones de enlace</span><span class="sxs-lookup"><span data-stu-id="56471-103">In-Context Hook Functions</span></span>

<span data-ttu-id="56471-104">En la siguiente lista se describen los aspectos clave de las funciones de enlace en contexto:</span><span class="sxs-lookup"><span data-stu-id="56471-104">The following list outlines the key aspects of in-context hook functions:</span></span>

-   <span data-ttu-id="56471-105">Las funciones de enlaces en contexto deben estar ubicadas en una biblioteca de vínculos dinámicos (DLL) que el sistema asigna al espacio de direcciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="56471-105">In-context hooks functions must be located in a dynamic-link library (DLL) that the system maps into the server's address space.</span></span>
-   <span data-ttu-id="56471-106">Las funciones de enlace en contexto comparten el espacio de direcciones con el servidor.</span><span class="sxs-lookup"><span data-stu-id="56471-106">In-context hook functions share the address space with the server.</span></span>
-   <span data-ttu-id="56471-107">Cuando el servidor desencadena un evento, el sistema llama a una función de enlace sin serialización (empaquetado y envío de parámetros de interfaz a través de los límites del proceso).</span><span class="sxs-lookup"><span data-stu-id="56471-107">When the server triggers an event, the system calls a hook function without marshaling (packaging and sending interface parameters across process boundaries).</span></span>
-   <span data-ttu-id="56471-108">Las funciones de enlace en contexto suelen ser muy rápidas y reciben notificaciones de eventos sincrónicamente porque no hay ningún cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="56471-108">In-context hook functions tend to be very fast and receive event notifications synchronously because there is no marshaling.</span></span>
-   <span data-ttu-id="56471-109">Es posible que algunos eventos se entreguen fuera de proceso, aunque solicite que se entreguen en proceso (mediante la \_ marca de INCONTEXTO WINEVENT).</span><span class="sxs-lookup"><span data-stu-id="56471-109">Some events may be delivered out-of-process, even though you request that they be delivered in-process (using the WINEVENT\_INCONTEXT flag).</span></span> <span data-ttu-id="56471-110">Podría ver esta situación con problemas de interoperabilidad de aplicaciones de 64 y 32 bits y con eventos de la consola de Windows.</span><span class="sxs-lookup"><span data-stu-id="56471-110">You might see this situation with 64-bit and 32-bit application interoperability issues and with Windows console events.</span></span>

 

 




