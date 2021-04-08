---
title: Proxy de servicio y sesiones
description: El proxy de servicio tiene comportamientos especiales para los enlaces de canal de sesión y no basados en sesión.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Servicios Web de proxy de servicio y sesiones para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078623"
---
# <a name="service-proxy-and-sessions"></a><span data-ttu-id="5f146-106">Proxy de servicio y sesiones</span><span class="sxs-lookup"><span data-stu-id="5f146-106">Service Proxy and Sessions</span></span>

<span data-ttu-id="5f146-107">El [proxy de servicio](service-proxy.md) tiene comportamientos especiales para los enlaces de canal de sesión y no basados en sesión.</span><span class="sxs-lookup"><span data-stu-id="5f146-107">The [service proxy](service-proxy.md) has special behaviors for session and non-session-based channel bindings.</span></span> <span data-ttu-id="5f146-108">El proxy de servicio proporciona semántica basada en sesión si el enlace de canal subyacente está basado en sesión.</span><span class="sxs-lookup"><span data-stu-id="5f146-108">The service proxy provides session based semantics if the underlying channel binding is session based.</span></span> <span data-ttu-id="5f146-109">En este caso, se utiliza un canal único para atender las llamadas.</span><span class="sxs-lookup"><span data-stu-id="5f146-109">In this case a single channel is used to service calls.</span></span> <span data-ttu-id="5f146-110">Sin embargo, si el enlace de canal no está basado en sesión, el proxy de servicio crea un canal independiente para cada llamada.</span><span class="sxs-lookup"><span data-stu-id="5f146-110">However, if the channel binding is not session based, the service proxy creates a separate channel for each call.</span></span> <span data-ttu-id="5f146-111">Sin embargo, tenga en cuenta que los canales no basados en sesión se agrupan y quizás se reutilizan.</span><span class="sxs-lookup"><span data-stu-id="5f146-111">Note, though, that non-session-based channels are pooled and maybe reused.</span></span> <span data-ttu-id="5f146-112">En la reutilización de un canal, el proxy de servicio mantiene el canal abierto si el canal subyacente no ha generado un error o la llamada en un canal ha dado lugar a un error en el canal del proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="5f146-112">In reusing a channel, the service proxy keeps the channel open if the underlying channel has not faulted or the call on a channel has resulted in the service proxy's faulting the channel.</span></span> <span data-ttu-id="5f146-113">Tenga en cuenta que.</span><span class="sxs-lookup"><span data-stu-id="5f146-113">Note that.</span></span> <span data-ttu-id="5f146-114">excepto en el caso de que se produzca un error, cuando se abre un canal se mantiene abierto mientras el proxy del servicio esté abierto y se cierre solo cuando se cierre el proxy del servicio.</span><span class="sxs-lookup"><span data-stu-id="5f146-114">except in the event of a fault, once a channel is opened it is kept open as long as the service proxy is open and is closed only when the service proxy is closed.</span></span>


<span data-ttu-id="5f146-115">Si el enlace de canal está basado en sesión y se produce un error en el canal subyacente, la máquina de Estados de proxy de servicio pasará al estado de [**error de estado de proxy de WS \_ Service \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="5f146-115">If the channel binding is session based and if the underlying channel faults, the service proxy state machine will transition into the [**WS\_SERVICE\_PROXY\_STATE\_FAULTED**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) state.</span></span> <span data-ttu-id="5f146-116">En el caso de un enlace de canal no basado en sesión, un error en el canal subyacente no hace que el proxy pase al estado de **error de estado de proxy de servicio de WS \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="5f146-116">In the case of non-session based channel binding, a fault in the underlying channel does not cause the proxy to transition into **WS\_SERVICE\_PROXY\_STATE\_FAULTED** state.</span></span>

<span data-ttu-id="5f146-117">Para obtener más información sobre el proxy del servicio y su relación con el estado, vea el tema [proxy del servicio](service-proxy.md) .</span><span class="sxs-lookup"><span data-stu-id="5f146-117">For more information on the service proxy and its relation to state, see the [Service Proxy](service-proxy.md) topic.</span></span> <span data-ttu-id="5f146-118">Para obtener ejemplos de diferentes enlaces de canal, vea los ejemplos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5f146-118">For examples of different channel bindings see the following examples:</span></span>

-   <span data-ttu-id="5f146-119">enlace de canal que no es de sesión, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="5f146-119">non-session channel binding, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span></span>
-   <span data-ttu-id="5f146-120">enlace de canal basado en sesión, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="5f146-120">session-based channel binding, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span></span>

 

 




