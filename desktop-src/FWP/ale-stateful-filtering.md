---
title: Filtrado con estado ALE
description: Los filtros instalados en las capas de aplicación de nivel de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) realizan el filtrado de red con estado.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077749"
---
# <a name="ale-stateful-filtering"></a><span data-ttu-id="7be4b-103">Filtrado con estado ALE</span><span class="sxs-lookup"><span data-stu-id="7be4b-103">ALE Stateful Filtering</span></span>

<span data-ttu-id="7be4b-104">Los filtros instalados en las capas de aplicación de nivel de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) realizan el filtrado de red con estado.</span><span class="sxs-lookup"><span data-stu-id="7be4b-104">Filters installed at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) perform stateful network filtering.</span></span> <span data-ttu-id="7be4b-105">Un *flujo de Ale* se utiliza como base para el filtrado con estado ALE.</span><span class="sxs-lookup"><span data-stu-id="7be4b-105">An *ALE flow* is used as the basis for ALE stateful filtering.</span></span>

<span data-ttu-id="7be4b-106">Un flujo ALE es una manera de clasificar el tráfico de red mediante su agrupación en función de una dirección IP de origen, una dirección IP de destino, un puerto de origen, un puerto de destino y un protocolo.</span><span class="sxs-lookup"><span data-stu-id="7be4b-106">An ALE flow is a way of classifying network traffic by grouping it based on a Source IP Address, a Destination IP Address, a Source Port, a Destination Port, and a Protocol.</span></span> <span data-ttu-id="7be4b-107">Un flujo ALE podría ser genérico, es decir, uno o varios de los descriptores podrían coincidir con todo (o con comodín \* ).</span><span class="sxs-lookup"><span data-stu-id="7be4b-107">An ALE flow could be generic, that is one or more of the descriptors could be matching everything (or wildcard \*).</span></span> <span data-ttu-id="7be4b-108">Por ejemplo, un flujo de ALE de UDP genérico se describiría como la dirección IP de origen = \* , la dirección IP de destino = \* , el puerto de origen =, el puerto de \* destino = \* y el protocolo = UDP.</span><span class="sxs-lookup"><span data-stu-id="7be4b-108">For example, a generic UDP ALE flow would be described as Source IP Address = \*, Destination IP Address = \*, Source Port = \*, Destination Port = \*, and Protocol = UDP.</span></span>

<span data-ttu-id="7be4b-109">Una vez que se autoriza una conexión (las conexiones entrantes están autorizadas en el nivel de FWPM de recepción de autenticación Ale de la capa de la versión de [**\_ \_ \_ \_ \_ aceptación \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) y las conexiones salientes en la capa de FWPM de la **\_ \_ \_ autenticación \_ \_ \| Ale** de la capa de), se crea un flujo ALE de modo que, con el bloqueo de un cambio de Directiva, todos los paquetes, entrantes y salientes, que pertenezcan al mismo flujo de Ale se permitan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7be4b-109">Once a connection is authorized (inbound connections are authorized at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and outbound connections at the **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layer), an ALE flow is created such that, barring a policy change, all packets, inbound and outbound, that belong to the same ALE flow are permitted automatically.</span></span> <span data-ttu-id="7be4b-110">Dado que un cambio de directiva podría requerir el bloqueo de conexiones permitidas previamente, los flujos de ALE deben [reautorizarse](ale-re-authorization.md) cuando se produce un cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="7be4b-110">Because a policy change might require blocking previously allowed connections, ALE flows need to be [reauthorized](ale-re-authorization.md) when a policy change occurs.</span></span>

<span data-ttu-id="7be4b-111">El filtrado con estado ALE reduce drásticamente el número de clasificaciones necesarias mediante la clasificación solo del primer paquete que pertenece a un flujo ALE.</span><span class="sxs-lookup"><span data-stu-id="7be4b-111">ALE stateful filtering reduces drastically the number of required classifications by classifying only the first packet that belongs to an ALE flow.</span></span> <span data-ttu-id="7be4b-112">Por comparación, el filtrado sin estado requiere la clasificación de cada paquete que atraviesa la red.</span><span class="sxs-lookup"><span data-stu-id="7be4b-112">By comparison, non-stateful filtering requires classification of every packet that traverse the network.</span></span>

<span data-ttu-id="7be4b-113">Un flujo ALE tiene una dirección asociada, que es la dirección del primer paquete del flujo.</span><span class="sxs-lookup"><span data-stu-id="7be4b-113">An ALE flow has an associated direction, which is the direction of the first packet of the flow.</span></span> <span data-ttu-id="7be4b-114">Esto permite directivas más flexibles, ya que permite que las conexiones iniciadas entrantes tengan diferentes directivas de las conexiones iniciadas salientes.</span><span class="sxs-lookup"><span data-stu-id="7be4b-114">This allows for more flexible policies, by permitting inbound initiated connections to have different policies from outbound initiated connections.</span></span>

## <a name="tcp-ale-flow"></a><span data-ttu-id="7be4b-115">Flujo ALE TCP</span><span class="sxs-lookup"><span data-stu-id="7be4b-115">TCP ALE Flow</span></span>

<span data-ttu-id="7be4b-116">Un flujo ALE para el tráfico TCP se identifica mediante la tupla de cinco de TCP/IP (dirección IP de origen, dirección IP de destino, Puerto de origen, Puerto de destino y Protocolo).</span><span class="sxs-lookup"><span data-stu-id="7be4b-116">An ALE flow for TCP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="7be4b-117">Un flujo ALE TCP tiene la misma duración que un socket TCP conectado.</span><span class="sxs-lookup"><span data-stu-id="7be4b-117">A TCP ALE flow has the same lifetime as a connected TCP socket.</span></span> <span data-ttu-id="7be4b-118">Un socket TCP conectado podría ser un socket creado mediante [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) o un socket creado como resultado de una llamada a [**accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) .</span><span class="sxs-lookup"><span data-stu-id="7be4b-118">A connected TCP socket could be either a socket created using [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) or a socket created as a result of an [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) call.</span></span>

<span data-ttu-id="7be4b-119">ALE mantiene una relación uno a uno entre un flujo ALE TCP y un bloque de control TCP (TCB).</span><span class="sxs-lookup"><span data-stu-id="7be4b-119">ALE maintains a one-to-one relationship between a TCP ALE flow and a TCP Control Block (TCB).</span></span>

## <a name="udp-ale-flow"></a><span data-ttu-id="7be4b-120">Flujo ALE UDP</span><span class="sxs-lookup"><span data-stu-id="7be4b-120">UDP ALE Flow</span></span>

> [!Note]  
> <span data-ttu-id="7be4b-121">Los protocolos que no son TCP o ICMP se tratan como UDP.</span><span class="sxs-lookup"><span data-stu-id="7be4b-121">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="7be4b-122">Un flujo ALE para el tráfico UDP se identifica mediante la tupla de cinco de TCP/IP (dirección IP de origen, dirección IP de destino, Puerto de origen, Puerto de destino y Protocolo).</span><span class="sxs-lookup"><span data-stu-id="7be4b-122">An ALE flow for UDP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="7be4b-123">Un flujo ALE UDP se crea basándose en un socket UDP y representa el elemento remoto del mismo nivel con el que se comunica la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7be4b-123">A UDP ALE flow is created based on a UDP socket and it represents the remote peer that the application is communicating with.</span></span> <span data-ttu-id="7be4b-124">Un elemento remoto del mismo nivel se identifica mediante una tupla (dirección IP de destino y puerto de destino).</span><span class="sxs-lookup"><span data-stu-id="7be4b-124">A remote peer is identified by a (Destination IP Address and Destination Port) tuple.</span></span>

<span data-ttu-id="7be4b-125">Existe una relación de uno a varios entre un socket UDP y los pares remotos a los que se comunica.</span><span class="sxs-lookup"><span data-stu-id="7be4b-125">There is a one-to-many relationship between a UDP socket and the remote peers that it talks to.</span></span>

<span data-ttu-id="7be4b-126">Cuando se cierra el socket UDP local, se eliminarán todos los flujos de ALE asociados a él.</span><span class="sxs-lookup"><span data-stu-id="7be4b-126">When the local UDP socket is closed, all the ALE flows associated with it will be deleted.</span></span>

<span data-ttu-id="7be4b-127">En ausencia de cierres de socket, los flujos ALE de unidifusión de UDP tienen un tiempo de espera de inactividad [configurable](ale-flow-customization.md) que tiene como valor predeterminado 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="7be4b-127">In the absence of socket closures, UDP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="7be4b-128">Si no se envía ni se recibe ningún paquete en esta ventana, se eliminará el flujo de ALE.</span><span class="sxs-lookup"><span data-stu-id="7be4b-128">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="7be4b-129">Este tiempo de espera predeterminado se acorta progresivamente cuando el número de flujos ALE en todo el sistema alcanza un umbral determinado.</span><span class="sxs-lookup"><span data-stu-id="7be4b-129">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

## <a name="icmp-ale-flow"></a><span data-ttu-id="7be4b-130">Flujo ALE de ICMP</span><span class="sxs-lookup"><span data-stu-id="7be4b-130">ICMP ALE Flow</span></span>

<span data-ttu-id="7be4b-131">Un flujo ALE para el tráfico ICMP se identifica mediante las seis tuplas (dirección IP de origen, dirección IP de destino, tipo de ICMP, Código ICMP, protocolo e ID. de ICMP).</span><span class="sxs-lookup"><span data-stu-id="7be4b-131">An ALE flow for ICMP traffic is identified by the six-tuple (Source IP Address, Destination IP Address, ICMP type, ICMP code, Protocol, and ICMP ID).</span></span> <span data-ttu-id="7be4b-132">El identificador de ICMP forma parte del flujo de ALE solo para el tráfico ICMP de eco y respuesta.</span><span class="sxs-lookup"><span data-stu-id="7be4b-132">The ICMP ID is part of the ALE flow only for ICMP echo/reply traffic.</span></span>

<span data-ttu-id="7be4b-133">En ausencia de cierres de socket, los flujos ALE de unidifusión ICMP tienen un tiempo de espera de inactividad [configurable](ale-flow-customization.md) cuyo valor predeterminado es de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="7be4b-133">In the absence of socket closures, ICMP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="7be4b-134">Si no se envía ni se recibe ningún paquete en esta ventana, se eliminará el flujo de ALE.</span><span class="sxs-lookup"><span data-stu-id="7be4b-134">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="7be4b-135">Este tiempo de espera predeterminado se acorta progresivamente cuando el número de flujos ALE en todo el sistema alcanza un umbral determinado.</span><span class="sxs-lookup"><span data-stu-id="7be4b-135">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

<span data-ttu-id="7be4b-136">Solo se indican los mensajes que no son de error de ICMP a las capas ALE.</span><span class="sxs-lookup"><span data-stu-id="7be4b-136">Only ICMP non-error messages are indicated to ALE layers.</span></span> <span data-ttu-id="7be4b-137">Los mensajes de error de ICMP se pueden inspeccionar en capas de error de ICMP \_ .</span><span class="sxs-lookup"><span data-stu-id="7be4b-137">ICMP error messages can be inspected at ICMP\_ERROR layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7be4b-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7be4b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7be4b-139">Aplicación del nivel de aplicación (ALE)</span><span class="sxs-lookup"><span data-stu-id="7be4b-139">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="7be4b-140">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="7be4b-140">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="7be4b-141">Tráfico de multidifusión/difusión ALE</span><span class="sxs-lookup"><span data-stu-id="7be4b-141">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="7be4b-142">Reautorización de ALE</span><span class="sxs-lookup"><span data-stu-id="7be4b-142">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="7be4b-143">Personalización del flujo ALE</span><span class="sxs-lookup"><span data-stu-id="7be4b-143">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="7be4b-144">Flujos de paquetes TCP</span><span class="sxs-lookup"><span data-stu-id="7be4b-144">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="7be4b-145">Flujos de paquetes UDP</span><span class="sxs-lookup"><span data-stu-id="7be4b-145">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="7be4b-146">Funciones de Winsock</span><span class="sxs-lookup"><span data-stu-id="7be4b-146">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 