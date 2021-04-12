---
title: Registro con el administrador de tablas de enrutamiento
description: Para que un cliente pueda acceder a la tabla de enrutamiento, primero debe registrarse con el administrador de tablas de enrutamiento mediante la función RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Administrador de tablas de enrutamiento versión 2 RRAS, registrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268701"
---
# <a name="registering-with-the-routing-table-manager"></a><span data-ttu-id="286ac-104">Registro con el administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="286ac-104">Registering with the Routing Table Manager</span></span>

<span data-ttu-id="286ac-105">Para que un cliente pueda acceder a la tabla de enrutamiento, primero debe registrarse con el administrador de tablas de enrutamiento mediante la función [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) .</span><span class="sxs-lookup"><span data-stu-id="286ac-105">Before a client can access the routing table, it first must register with the routing table manager using the [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function.</span></span>

<span data-ttu-id="286ac-106">Cuando un cliente se registra, pasa a la estructura de información de la [**\_ \_ entidad RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="286ac-106">When a client registers, it passes to the routing table manager an [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structure.</span></span> <span data-ttu-id="286ac-107">Esta estructura contiene la información que identifica de forma única un cliente, la familia de direcciones y la instancia del administrador de tabla de enrutamiento con la que el cliente se registra.</span><span class="sxs-lookup"><span data-stu-id="286ac-107">This structure contains the information that uniquely identifies a client, the address family, and the instance of the routing table manager with which the client is registering.</span></span> <span data-ttu-id="286ac-108">Un cliente también puede establecer la devolución de llamada de [**\_ devolución de \_ llamada de evento de RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) .</span><span class="sxs-lookup"><span data-stu-id="286ac-108">A client can also establish the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback.</span></span> <span data-ttu-id="286ac-109">El administrador de tablas de enrutamiento usará esta devolución de llamada para notificar al cliente los eventos, como las notificaciones de cambio y los registros de cliente.</span><span class="sxs-lookup"><span data-stu-id="286ac-109">The routing table manager will use this callback to notify the client of events such as change notifications and client registrations.</span></span>

<span data-ttu-id="286ac-110">El administrador de tablas de enrutamiento completa su procesamiento de registro y devuelve un identificador al cliente.</span><span class="sxs-lookup"><span data-stu-id="286ac-110">The routing table manager completes its registration processing and returns a handle to the client.</span></span> <span data-ttu-id="286ac-111">El cliente debe utilizar este identificador para todas las llamadas subsiguientes a las funciones de RTMv2.</span><span class="sxs-lookup"><span data-stu-id="286ac-111">The client must use this handle for all subsequent calls to RTMv2 functions.</span></span>

<span data-ttu-id="286ac-112">La función [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) que se usa en RTMv2 es análoga a la función [**RtmRegisterClient**](rtmregisterclient.md) que se usa en RTMv1.</span><span class="sxs-lookup"><span data-stu-id="286ac-112">The [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function that is used in RTMv2 is analogous to the [**RtmRegisterClient**](rtmregisterclient.md) function that is used in RTMv1.</span></span> <span data-ttu-id="286ac-113">La función **RtmRegisterClient** está obsoleta, excepto los clientes que usan IPX.</span><span class="sxs-lookup"><span data-stu-id="286ac-113">The **RtmRegisterClient** function is obsolete, except for clients using IPX.</span></span>

<span data-ttu-id="286ac-114">Una vez que un cliente ha terminado de interactuar con el administrador de tablas de enrutamiento, debe llamar a [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span><span class="sxs-lookup"><span data-stu-id="286ac-114">Once a client has finished interacting with the routing table manager, it must call [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span></span> <span data-ttu-id="286ac-115">El administrador de tablas de enrutamiento destruye el identificador asociado con el cliente.</span><span class="sxs-lookup"><span data-stu-id="286ac-115">The routing table manager destroys the handle associated with the client.</span></span> <span data-ttu-id="286ac-116">Para evitar pérdidas de memoria, el cliente debe asegurarse de que libera todos los identificadores y elimina todas las rutas y los próximos saltos que posee antes de llamar a **RtmDeregisterEntity**.</span><span class="sxs-lookup"><span data-stu-id="286ac-116">To avoid memory leaks, the client must ensure that it releases all handles and deletes all the routes and next hops that it owns before calling **RtmDeregisterEntity**.</span></span>

<span data-ttu-id="286ac-117">Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [registrar con el administrador de tablas de enrutamiento](register-with-the-routing-table-manager.md) y [usar la devolución de llamada de notificación de eventos](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="286ac-117">For sample code that shows how to use these functions, see [Register with the Routing Table Manager](register-with-the-routing-table-manager.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




