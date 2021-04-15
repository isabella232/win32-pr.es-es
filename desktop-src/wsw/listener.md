---
title: Agente de escucha
description: El cliente utiliza un agente de escucha para aceptar un canal entrante de un servicio.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Servicios web del agente de escucha para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421644"
---
# <a name="listener"></a><span data-ttu-id="f2439-106">Agente de escucha</span><span class="sxs-lookup"><span data-stu-id="f2439-106">Listener</span></span>

<span data-ttu-id="f2439-107">El cliente utiliza un agente de escucha para aceptar un [canal](channel.md) entrante de un servicio.</span><span class="sxs-lookup"><span data-stu-id="f2439-107">A listener is used by the client to accept an incoming [channel](channel.md) from a service.</span></span>

<span data-ttu-id="f2439-108">Para crear un agente, debe especificar el tipo de canal como un valor de enumeración de [**\_ \_ tipo de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , la información de [enlace](binding.md) y la [dirección URL](url.md) en la que se va a escuchar.</span><span class="sxs-lookup"><span data-stu-id="f2439-108">To create a listner, you specify the channel type as a [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) enumeration value, the [binding](binding.md) information, and the [URL](url.md) to listen on.</span></span>


<span data-ttu-id="f2439-109">Para empezar a escuchar en la dirección URL, llame a la función [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .</span><span class="sxs-lookup"><span data-stu-id="f2439-109">To start listening on the URL, call the [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) function.</span></span>

<span data-ttu-id="f2439-110">Para aceptar las comunicaciones entrantes, llame a [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span><span class="sxs-lookup"><span data-stu-id="f2439-110">To accept incoming communications, call [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span></span>

<span data-ttu-id="f2439-111">Para cancelar la e/s pendiente para un agente de escucha, llame a [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span><span class="sxs-lookup"><span data-stu-id="f2439-111">To cancel pending IO for a listener, call [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span></span>

<span data-ttu-id="f2439-112">Para obtener información sobre las transiciones de estado de un agente de escucha, vea la enumeración de [**\_ \_ Estado de escucha de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .</span><span class="sxs-lookup"><span data-stu-id="f2439-112">For information on the state transitions for a listener, see the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) enumeration.</span></span>

<span data-ttu-id="f2439-113">Las siguientes devoluciones de llamada forman parte del agente de escucha:</span><span class="sxs-lookup"><span data-stu-id="f2439-113">The following callbacks are part of the listener:</span></span>

-   [<span data-ttu-id="f2439-114">**\_devolución de \_ llamada de agente de escucha de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-114">**WS\_ABORT\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [<span data-ttu-id="f2439-115">**\_devolución de \_ llamada de canal de aceptación de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-115">**WS\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [<span data-ttu-id="f2439-116">**\_devolución de \_ llamada del agente de escucha de WS Close \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-116">**WS\_CLOSE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [<span data-ttu-id="f2439-117">**WS \_ Create \_ Channel \_ para \_ devolución de llamada del agente de escucha \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-117">**WS\_CREATE\_CHANNEL\_FOR\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [<span data-ttu-id="f2439-118">**\_devolución de \_ llamada de agente de escucha de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-118">**WS\_CREATE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [<span data-ttu-id="f2439-119">**\_devolución de \_ llamada de agente de escucha gratuito de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-119">**WS\_FREE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [<span data-ttu-id="f2439-120">**\_devolución de \_ llamada de \_ propiedad de agente de escucha de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-120">**WS\_GET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [<span data-ttu-id="f2439-121">**\_devolución de \_ llamada de agente de escucha abierto WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-121">**WS\_OPEN\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [<span data-ttu-id="f2439-122">**\_devolución de \_ llamada del agente de escucha de WS RESET \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-122">**WS\_RESET\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [<span data-ttu-id="f2439-123">**\_devolución de \_ llamada de \_ propiedad del agente de escucha de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-123">**WS\_SET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

<span data-ttu-id="f2439-124">Las enumeraciones siguientes forman parte del agente de escucha:</span><span class="sxs-lookup"><span data-stu-id="f2439-124">The following enumerations are part of the listener:</span></span>

-   [<span data-ttu-id="f2439-125">**versión de WS \_ IP \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-125">**WS\_IP\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [<span data-ttu-id="f2439-126">**identificador de la propiedad del agente de escucha de WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-126">**WS\_LISTENER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [<span data-ttu-id="f2439-127">**\_Estado del agente de escucha de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-127">**WS\_LISTENER\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

<span data-ttu-id="f2439-128">Las siguientes funciones forman parte del agente de escucha:</span><span class="sxs-lookup"><span data-stu-id="f2439-128">The following functions are part of the listener:</span></span>

-   [<span data-ttu-id="f2439-129">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="f2439-129">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [<span data-ttu-id="f2439-130">**WsAcceptChannel**</span><span class="sxs-lookup"><span data-stu-id="f2439-130">**WsAcceptChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [<span data-ttu-id="f2439-131">**WsCloseListener**</span><span class="sxs-lookup"><span data-stu-id="f2439-131">**WsCloseListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [<span data-ttu-id="f2439-132">**WsCreateListener**</span><span class="sxs-lookup"><span data-stu-id="f2439-132">**WsCreateListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [<span data-ttu-id="f2439-133">**WsFreeListener**</span><span class="sxs-lookup"><span data-stu-id="f2439-133">**WsFreeListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [<span data-ttu-id="f2439-134">**WsGetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="f2439-134">**WsGetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [<span data-ttu-id="f2439-135">**WsOpenListener**</span><span class="sxs-lookup"><span data-stu-id="f2439-135">**WsOpenListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [<span data-ttu-id="f2439-136">**WsResetListener**</span><span class="sxs-lookup"><span data-stu-id="f2439-136">**WsResetListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [<span data-ttu-id="f2439-137">**WsSetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="f2439-137">**WsSetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

<span data-ttu-id="f2439-138">El siguiente identificador forma parte del agente de escucha:</span><span class="sxs-lookup"><span data-stu-id="f2439-138">The following handle is part of the listener:</span></span>

-   [<span data-ttu-id="f2439-139">agente de escucha de WS \_</span><span class="sxs-lookup"><span data-stu-id="f2439-139">WS\_LISTENER</span></span>](ws-listener.md)

<span data-ttu-id="f2439-140">Las siguientes estructuras forman parte del agente de escucha:</span><span class="sxs-lookup"><span data-stu-id="f2439-140">The following structures are part of the listener:</span></span>

-   [<span data-ttu-id="f2439-141">**\_devoluciones de llamada de agente de escucha personalizado de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-141">**WS\_CUSTOM\_LISTENER\_CALLBACKS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [<span data-ttu-id="f2439-142">**no se \_ permiten \_ \_ subcadenas de agente de usuario \_ de WS**</span><span class="sxs-lookup"><span data-stu-id="f2439-142">**WS\_DISALLOWED\_USER\_AGENT\_SUBSTRINGS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [<span data-ttu-id="f2439-143">**\_nombres de host de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-143">**WS\_HOST\_NAMES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [<span data-ttu-id="f2439-144">**\_propiedades del agente de escucha de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-144">**WS\_LISTENER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [<span data-ttu-id="f2439-145">**\_propiedad del agente de escucha de WS \_**</span><span class="sxs-lookup"><span data-stu-id="f2439-145">**WS\_LISTENER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




