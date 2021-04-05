---
title: Cancelación
description: La mayoría de las operaciones de WWSAPI se pueden cancelar durante la ejecución.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Servicios Web de cancelación para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359545"
---
# <a name="cancellation"></a><span data-ttu-id="6f58a-106">Cancelación</span><span class="sxs-lookup"><span data-stu-id="6f58a-106">Cancellation</span></span>

<span data-ttu-id="6f58a-107">La mayoría de las operaciones de WWSAPI se pueden cancelar durante la ejecución.</span><span class="sxs-lookup"><span data-stu-id="6f58a-107">Most of operations in the WWSAPI can be canceled during execution.</span></span>

<span data-ttu-id="6f58a-108">La función que se usa para cancelar una operación depende del objeto afectado.</span><span class="sxs-lookup"><span data-stu-id="6f58a-108">Which function you use to cancel an operation depends on the object affected.</span></span>

| <span data-ttu-id="6f58a-109">Función</span><span class="sxs-lookup"><span data-stu-id="6f58a-109">Function</span></span>                                           | <span data-ttu-id="6f58a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f58a-110">Description</span></span>                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f58a-111">**WsAbortChannel**</span><span class="sxs-lookup"><span data-stu-id="6f58a-111">**WsAbortChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | <span data-ttu-id="6f58a-112">Cancela todas las entradas y salidas pendientes en un canal especificado y establece el estado del canal en estado de canal de WS con \_ \_ \_ errores.</span><span class="sxs-lookup"><span data-stu-id="6f58a-112">Cancels all pending input and output on a specified channel and sets the channel state to WS\_CHANNEL\_STATE\_FAULTED.</span></span> |
| [<span data-ttu-id="6f58a-113">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="6f58a-113">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | <span data-ttu-id="6f58a-114">Cancela todas las entradas y salidas pendientes en un agente de escucha especificado.</span><span class="sxs-lookup"><span data-stu-id="6f58a-114">Cancels all pending input and output on a specified listener.</span></span>                                                          |
| [<span data-ttu-id="6f58a-115">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="6f58a-115">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | <span data-ttu-id="6f58a-116">Cancela todas las entradas y salidas pendientes en un proxy de servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="6f58a-116">Cancels all pending input and output on a specified service proxy.</span></span>                                                     |
| [<span data-ttu-id="6f58a-117">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="6f58a-117">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | <span data-ttu-id="6f58a-118">Interrumpe y suspende las operaciones actuales en el host de servicio.</span><span class="sxs-lookup"><span data-stu-id="6f58a-118">Interrupts and discontinues current operations on the service host.</span></span>                                                    |
| [<span data-ttu-id="6f58a-119">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="6f58a-119">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | <span data-ttu-id="6f58a-120">Abandona una llamada a, una llamada especificada en un proxy de servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="6f58a-120">Abandons a call, a specified call on a specified service proxy.</span></span>                                                        |



 

<span data-ttu-id="6f58a-121">Para obtener información sobre las cancelaciones que afectan a [las operaciones de servicio del lado servidor y las](server-side-service-operations.md) devoluciones de llamada del modelo de servicio, consulte [cancelación de llamadas](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="6f58a-121">For information on cancellations that affect [server side service operations](server-side-service-operations.md) and service-model callbacks, see [Call Cancellation](call-cancellation.md).</span></span>


 

 




