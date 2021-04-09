---
title: Consideraciones sobre la programación de MGM
description: 'Al desarrollar clientes de administrador de grupo de multidifusión, siga las directrices siguientes:'
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multidifusión, consideraciones de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903654"
---
# <a name="mgm-programming-considerations"></a><span data-ttu-id="40049-104">Consideraciones sobre la programación de MGM</span><span class="sxs-lookup"><span data-stu-id="40049-104">MGM Programming Considerations</span></span>

<span data-ttu-id="40049-105">Al desarrollar clientes de administrador de grupo de multidifusión, observe las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="40049-105">When you are developing multicast group manager clients, observe the following guidelines:</span></span>

-   <span data-ttu-id="40049-106">Las llamadas a funciones se deben realizar desde dentro del proceso del enrutador.</span><span class="sxs-lookup"><span data-stu-id="40049-106">Function calls must be made from within the router process.</span></span> <span data-ttu-id="40049-107">Si se llama a las funciones desde otro proceso, sus resultados no serán válidos; el cliente no interactuará con el administrador del grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="40049-107">If functions are called from another process, their results will not be valid; the client will not interact with the multicast group manager.</span></span>
-   <span data-ttu-id="40049-108">Los clientes que usan la API MGM deben proporcionar su propia comprobación de errores, asegurándose de que solo se pasan datos válidos al administrador del grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="40049-108">Clients that use the MGM API must provide their own error checking, ensuring that only valid data is passed to the multicast group manager.</span></span> <span data-ttu-id="40049-109">Las funciones MGM no devuelven mensajes de error detallados sobre parámetros no válidos. el valor del parámetro de ERROR \_ no válido \_ se devuelve sin explicación.</span><span class="sxs-lookup"><span data-stu-id="40049-109">MGM functions do not return detailed error messages about invalid parameters; the ERROR\_INVALID\_PARAMETER value is returned without explanation.</span></span>
-   <span data-ttu-id="40049-110">Los clientes deben tener cuidado al utilizar los bloqueos mientras llaman a las funciones MGM.</span><span class="sxs-lookup"><span data-stu-id="40049-110">Clients should exercise caution in using locks while calling MGM functions.</span></span> <span data-ttu-id="40049-111">Si lo hace, puede evitar interbloqueos.</span><span class="sxs-lookup"><span data-stu-id="40049-111">Doing so can prevent deadlocks.</span></span> <span data-ttu-id="40049-112">Al llamar a las funciones MGM, los clientes no deben mantener los bloqueos que podrían mantenerse simultáneamente en una devolución de llamada del administrador del grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="40049-112">When calling MGM functions, clients should not hold any locks that might simultaneously be held in a callback from the multicast group manager.</span></span>

 

 




