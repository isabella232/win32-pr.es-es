---
title: Usar métodos
description: Cuando un cliente se registra con el administrador de tablas de enrutamiento, puede exportar un conjunto de métodos. Otros clientes usan estos métodos para obtener información específica del cliente. Los métodos permiten la comunicación privada entre los clientes del administrador de tablas de enrutamiento.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994309"
---
# <a name="using-methods"></a><span data-ttu-id="aeebb-105">Usar métodos</span><span class="sxs-lookup"><span data-stu-id="aeebb-105">Using Methods</span></span>

<span data-ttu-id="aeebb-106">Cuando un cliente se registra con el administrador de tablas de enrutamiento, puede exportar un conjunto de métodos.</span><span class="sxs-lookup"><span data-stu-id="aeebb-106">When a client registers with the routing table manager, it can export a set of methods.</span></span> <span data-ttu-id="aeebb-107">Otros clientes usan estos métodos para obtener información específica del cliente.</span><span class="sxs-lookup"><span data-stu-id="aeebb-107">These methods are used by other clients to obtain client-specific information.</span></span> <span data-ttu-id="aeebb-108">Los métodos permiten la comunicación privada entre los clientes del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="aeebb-108">Methods enable private communication between clients of the routing table manager.</span></span>

<span data-ttu-id="aeebb-109">Un cliente puede obtener la lista de métodos exportados por otro cliente.</span><span class="sxs-lookup"><span data-stu-id="aeebb-109">A client can obtain the list of methods exported by another client.</span></span> <span data-ttu-id="aeebb-110">El cliente llama a la función [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) , proporcionando el identificador del cliente de destino.</span><span class="sxs-lookup"><span data-stu-id="aeebb-110">The client calls the [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) function, supplying the target client's handle.</span></span>

<span data-ttu-id="aeebb-111">Cada método exportado por un cliente se identifica de forma única mediante su identificador de método.</span><span class="sxs-lookup"><span data-stu-id="aeebb-111">Each method exported by a client is uniquely identified by its method identifier.</span></span> <span data-ttu-id="aeebb-112">Cada cliente puede exportar hasta 32 métodos.</span><span class="sxs-lookup"><span data-stu-id="aeebb-112">Each client can export up to 32 methods.</span></span> <span data-ttu-id="aeebb-113">Cada método corresponde a un bit establecido en el miembro **MethodType** de la estructura de método de exportación de la [**\_ entidad \_ \_ RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) .</span><span class="sxs-lookup"><span data-stu-id="aeebb-113">Each method corresponds to a bit set in the **MethodType** member of the [**RTM\_ENTITY\_EXPORT\_METHOD**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) structure.</span></span> <span data-ttu-id="aeebb-114">Para invocar varios métodos, el cliente debe realizar una operación OR lógica de los identificadores para esos métodos.</span><span class="sxs-lookup"><span data-stu-id="aeebb-114">To invoke multiple methods, the client should perform a logical OR of the identifiers for those methods.</span></span> <span data-ttu-id="aeebb-115">La sintaxis y la semántica de las estructuras de entrada y salida de cada protocolo deben especificarse cuando se implementa el protocolo.</span><span class="sxs-lookup"><span data-stu-id="aeebb-115">The syntax and semantics of input and output structures for each protocol must be specified when the protocol is implemented.</span></span>

> [!Note]  
> <span data-ttu-id="aeebb-116">Microsoft reserva los valores de identificador de método que corresponden a un bit establecido en la mitad inferior del miembro **MethodType** (los 16 bits inferiores).</span><span class="sxs-lookup"><span data-stu-id="aeebb-116">Method identifier values that correspond to a bit set in the lower half of the **MethodType** member (the lower 16 bits) are reserved by Microsoft.</span></span>

 

<span data-ttu-id="aeebb-117">Para invocar el método de un segundo cliente, un cliente llama a la función [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) .</span><span class="sxs-lookup"><span data-stu-id="aeebb-117">To invoke a second client's method, a client calls the [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) function.</span></span> <span data-ttu-id="aeebb-118">El administrador de tablas de enrutamiento arbitra todas las solicitudes para invocar los métodos de un cliente.</span><span class="sxs-lookup"><span data-stu-id="aeebb-118">The routing table manager arbitrates all requests to invoke a client's methods.</span></span> <span data-ttu-id="aeebb-119">El administrador de tablas de enrutamiento realiza dos funciones cuando se arbitra entre clientes:</span><span class="sxs-lookup"><span data-stu-id="aeebb-119">The routing table manager performs two functions when it arbitrates between clients:</span></span>

-   <span data-ttu-id="aeebb-120">Evitar que el segundo cliente invoque un método para un cliente que está anulando el registro.</span><span class="sxs-lookup"><span data-stu-id="aeebb-120">Preventing the second client from invoking a method for a client that is unregistering.</span></span>
-   <span data-ttu-id="aeebb-121">Mantener una solicitud "Invoke" cuando se bloquean los métodos y permitir que la solicitud continúe cuando se desbloqueen los métodos.</span><span class="sxs-lookup"><span data-stu-id="aeebb-121">Holding an "invoke" request when methods are blocked, and allowing the request to continue when the methods are unblocked.</span></span>

<span data-ttu-id="aeebb-122">Si un cliente debe impedir que otros clientes ejecuten sus métodos, el cliente puede llamar a [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span><span class="sxs-lookup"><span data-stu-id="aeebb-122">If a client must prevent other clients from executing its methods, the client can call [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span></span> <span data-ttu-id="aeebb-123">El administrador de tablas de enrutamiento no permitirá que se procese una llamada a [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) hasta que el cliente desbloquee de nuevo sus métodos.</span><span class="sxs-lookup"><span data-stu-id="aeebb-123">The routing table manager will not allow a call to [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) to be processed until the client unblocks its methods again.</span></span>

<span data-ttu-id="aeebb-124">Normalmente, los clientes bloquean los métodos al realizar cambios en los datos privados que se intercambian entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="aeebb-124">Clients typically block methods when making changes to the private data that is exchanged between clients.</span></span> <span data-ttu-id="aeebb-125">Los métodos de bloqueo son una acción opcional.</span><span class="sxs-lookup"><span data-stu-id="aeebb-125">Blocking methods is an optional action.</span></span> <span data-ttu-id="aeebb-126">Un cliente también puede usar bloqueos internos para evitar que otros clientes invoquen métodos.</span><span class="sxs-lookup"><span data-stu-id="aeebb-126">A client can also use internal locks to prevent other clients from invoking methods.</span></span>

<span data-ttu-id="aeebb-127">Para ver el código de ejemplo que muestra cómo usar estas funciones, vea [obtener y llamar a los métodos exportados para un cliente](obtain-and-call-the-exported-methods-for-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="aeebb-127">For sample code that shows how to use these functions, see [Obtain and Call the Exported Methods for a Client](obtain-and-call-the-exported-methods-for-a-client.md).</span></span>

 

 




