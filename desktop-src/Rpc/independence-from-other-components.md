---
title: Independencia de otros componentes
description: Los datos de error extendidos son útiles incluso cuando el servidor o la aplicación a través de la que se ha pasado la cadena no reconoce los datos de error extendidos o no se aprovecha de él. Al final de esta sección se proporcionan enfoques recomendados para estas situaciones.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Independencia de otros componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994517"
---
# <a name="independence-from-other-components"></a><span data-ttu-id="e38fb-105">Independencia de otros componentes</span><span class="sxs-lookup"><span data-stu-id="e38fb-105">Independence From Other Components</span></span>

<span data-ttu-id="e38fb-106">Los datos de error extendidos son útiles incluso cuando el servidor o la aplicación a través de la que se ha pasado la cadena no reconoce los datos de error extendidos o no se aprovecha de él.</span><span class="sxs-lookup"><span data-stu-id="e38fb-106">Extended error data is useful even when the server or application through which the chain passed does not recognize extended error data, or does not take advantage of it.</span></span> <span data-ttu-id="e38fb-107">Al final de esta sección se proporcionan enfoques recomendados para estas situaciones.</span><span class="sxs-lookup"><span data-stu-id="e38fb-107">Recommended approaches for such situations are provided at the end of this section.</span></span>

<span data-ttu-id="e38fb-108">Los datos de error extendidos son muy útiles cuando las aplicaciones o los servidores que usan RPC aprovechan la información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="e38fb-108">Extended error data is most useful when applications or servers using RPC take advantage of extended error information.</span></span> <span data-ttu-id="e38fb-109">Al investigar un código de error de RPC \_ S \_ \* y los servidores o las aplicaciones implicadas no hacen que los datos de error extendidos estén disponibles, tenga en cuenta los siguientes enfoques:</span><span class="sxs-lookup"><span data-stu-id="e38fb-109">When investigating an RPC\_S\_\* error code and the servers or applications involved do not make extended error data available, consider the following approaches:</span></span>

-   <span data-ttu-id="e38fb-110">Realice un examen.</span><span class="sxs-lookup"><span data-stu-id="e38fb-110">Take a sniff.</span></span>

    <span data-ttu-id="e38fb-111">Reproduzca el escenario mientras realiza el examen.</span><span class="sxs-lookup"><span data-stu-id="e38fb-111">Reproduce the scenario while taking the sniff.</span></span> <span data-ttu-id="e38fb-112">El examen de la conexión contendrá los datos de error extendidos.</span><span class="sxs-lookup"><span data-stu-id="e38fb-112">The sniff of the wire will contain the extended error data.</span></span>

-   <span data-ttu-id="e38fb-113">Examínelo desde el depurador.</span><span class="sxs-lookup"><span data-stu-id="e38fb-113">Examine it from the debugger.</span></span>

    <span data-ttu-id="e38fb-114">Si no funciona el examen del problema, porque la llamada es local o porque el error se origina localmente, asocia un depurador al proceso que devuelve el error y coloca un punto de interrupción inmediatamente después de la llamada RPC que genera el error.</span><span class="sxs-lookup"><span data-stu-id="e38fb-114">If taking a sniff of the problem does not work, because the call is local or because the error originates locally, attach a debugger to the process returning the error and put a breakpoint immediately after the RPC call generating the error.</span></span> <span data-ttu-id="e38fb-115">RPC suele indicar errores iniciando excepciones, por lo que si busca el error 1825 (error de paquete de RPC \_ s \_ \_ \_ ), habilite la excepción 1825 y cuando el depurador se interrumpa en esa excepción, examine la información de error extendida para el subproceso.</span><span class="sxs-lookup"><span data-stu-id="e38fb-115">RPC often indicates errors by throwing exceptions, so if you are looking for error 1825 (RPC\_S\_SEC\_PKG\_ERROR), enable exception 1825 and when the debugger breaks on that exception, examine the extended error information for the thread.</span></span>

 

 




