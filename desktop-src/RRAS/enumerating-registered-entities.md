---
title: Enumerar entidades registradas
description: Una vez registrado un cliente, el cliente puede obtener una lista de todos los demás clientes registrados con el administrador de tablas de enrutamiento. Algunos clientes deben realizar ciertas operaciones si se detecta la presencia de un tipo de cliente determinado.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075773"
---
# <a name="enumerating-registered-entities"></a><span data-ttu-id="8a55f-104">Enumerar entidades registradas</span><span class="sxs-lookup"><span data-stu-id="8a55f-104">Enumerating Registered Entities</span></span>

<span data-ttu-id="8a55f-105">Una vez registrado un cliente, el cliente puede obtener una lista de todos los demás clientes registrados con el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="8a55f-105">After a client has registered, the client can obtain a list of all the other clients that have registered with the routing table manager.</span></span> <span data-ttu-id="8a55f-106">Algunos clientes deben realizar ciertas operaciones si se detecta la presencia de un tipo de cliente determinado.</span><span class="sxs-lookup"><span data-stu-id="8a55f-106">Some clients must perform certain operations if the presence of a particular type of client is detected.</span></span>

<span data-ttu-id="8a55f-107">El cliente puede llamar a la función [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) .</span><span class="sxs-lookup"><span data-stu-id="8a55f-107">The client can call the [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) function.</span></span> <span data-ttu-id="8a55f-108">Se devuelve un búfer de estructuras de [**\_ \_ información de entidad RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) .</span><span class="sxs-lookup"><span data-stu-id="8a55f-108">A buffer of [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structures is returned.</span></span> <span data-ttu-id="8a55f-109">Después de que el cliente haya procesado esta información, el cliente debe llamar a [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) para liberar los identificadores de las estructuras de información de la **\_ entidad \_ RTM** .</span><span class="sxs-lookup"><span data-stu-id="8a55f-109">After the client has processed this information, the client should call [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) to release the handles in the **RTM\_ENTITY\_INFO** structures.</span></span>

<span data-ttu-id="8a55f-110">Si el cliente del administrador de tablas de enrutamiento proporcionó una función de devolución de llamada en la llamada a [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), el cliente recibe una notificación cuando otros clientes registran o anulan el registro.</span><span class="sxs-lookup"><span data-stu-id="8a55f-110">If the routing table manager client supplied a callback function in the call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), the client is notified when any other clients register or unregister.</span></span>

<span data-ttu-id="8a55f-111">Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [enumerar las entidades registradas](enumerate-the-registered-entities.md) y [usar la devolución de llamada de notificación de eventos](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="8a55f-111">For sample code that shows how to use these functions, see [Enumerate the Registered Entities](enumerate-the-registered-entities.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




