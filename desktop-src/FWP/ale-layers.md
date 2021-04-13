---
title: Niveles ALE
description: El cumplimiento del nivel de aplicación (ALE) consta de varios niveles de filtrado y muchas capas de descarte coincidentes.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358836"
---
# <a name="ale-layers"></a><span data-ttu-id="19d09-103">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="19d09-103">ALE Layers</span></span>

<span data-ttu-id="19d09-104">El cumplimiento del nivel de aplicación (ALE) consta de varias capas de filtrado y muchas capas de descarte coincidentes.</span><span class="sxs-lookup"><span data-stu-id="19d09-104">The Application Layer Enforcement (ALE) consists of several filtering layers and many matching discard layers.</span></span> <span data-ttu-id="19d09-105">Todas las capas del motor de filtrado de la plataforma de filtrado de Windows (WFP), incluida la EPA, se describen en [**filtrar los identificadores de capas**](management-filtering-layer-identifiers-.md).</span><span class="sxs-lookup"><span data-stu-id="19d09-105">All the Windows Filtering Platform (WFP) filtering engine layers, including ALE, are described in [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md).</span></span> <span data-ttu-id="19d09-106">Este tema contiene una descripción más detallada de las capas de filtrado que forman parte de ALE.</span><span class="sxs-lookup"><span data-stu-id="19d09-106">This topic contains a more detailed description of the filtering layers that are part of ALE.</span></span>

## <a name="resource_assignment"></a><span data-ttu-id="19d09-107">asignación de recursos \_</span><span class="sxs-lookup"><span data-stu-id="19d09-107">RESOURCE\_ASSIGNMENT</span></span>

<span data-ttu-id="19d09-108">Un filtro en la capa de [**FWPM de \_ asignación de \_ \_ recursos Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las operaciones de enlace de red, explícita o implícita.</span><span class="sxs-lookup"><span data-stu-id="19d09-108">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for network bind operations, explicit or implicit.</span></span>

<span data-ttu-id="19d09-109">Si se compara un filtro en este nivel para autorizar la creación de un socket sin procesar, se establecerá la [**marca de condición de FWP \_ \_ \_ \_ sin formato \_**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="19d09-109">If a filter at this layer is matched to authorize raw socket creation, the [**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**](filtering-condition-flags-.md) flag will be set.</span></span>

<span data-ttu-id="19d09-110">Si se compara un filtro en este nivel para autorizar la recepción del modo promiscuo, el campo del [**\_ \_ \_ \_ modo promiscuo**](filtering-condition-identifiers-.md) de la condición de FWP se establecerá en SiO \_ RCVALL.</span><span class="sxs-lookup"><span data-stu-id="19d09-110">If a filter at this layer is matched to authorize promiscuous mode receiving, the [**FWP\_CONDITION\_ALE\_PROMISCUOUS\_MODE**](filtering-condition-identifiers-.md) field will be set to SIO\_RCVALL.</span></span> <span data-ttu-id="19d09-111">Para obtener una descripción de SIO \_ RCVALL, consulte [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span><span class="sxs-lookup"><span data-stu-id="19d09-111">For a description of SIO\_RCVALL, see [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span></span>

> [!Note]  
> <span data-ttu-id="19d09-112">Esta es la única capa en la que se puede filtrar el modo promiscuo.</span><span class="sxs-lookup"><span data-stu-id="19d09-112">This is the only layer where promiscuous mode can be filtered.</span></span>

 

<span data-ttu-id="19d09-113">Si no se especifica ningún puerto durante el **enlace ()**, es decir, el puerto se establece en 0 (cero), la pila TCP/IP seleccionará un puerto del intervalo de puertos dinámicos (19152 – 65535).</span><span class="sxs-lookup"><span data-stu-id="19d09-113">If no port is specified during **bind()**, that is, port is set to 0 (zero), then the TCP/IP stack will select a port from the dynamic port range (19152–65535).</span></span> <span data-ttu-id="19d09-114">El puerto seleccionado se clasificará en este nivel junto con la marca de condición de FWP como marca de [**\_ \_ \_ \_ \_ enlace de comodín**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="19d09-114">The selected port will be classified at this layer along with the [**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**](filtering-condition-flags-.md) flag.</span></span>

<span data-ttu-id="19d09-115">Si la dirección local no se especifica en la llamada [**BIND ()**](/windows/desktop/api/winsock/nf-winsock-bind) , el campo dirección local se establece en el valor de [**FWP \_ vacío**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="19d09-115">If the local address is not specified in the [**bind()**](/windows/desktop/api/winsock/nf-winsock-bind) call, the local address field is set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span>

## <a name="auth_listen"></a><span data-ttu-id="19d09-116">Escucha de autenticación \_</span><span class="sxs-lookup"><span data-stu-id="19d09-116">AUTH\_LISTEN</span></span>

<span data-ttu-id="19d09-117">Un filtro en la capa de [**FWPM de \_ escucha de \_ \_ autenticación Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las llamadas de escucha de TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-listen) .</span><span class="sxs-lookup"><span data-stu-id="19d09-117">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen) calls.</span></span>

## <a name="auth_recv_accept"></a><span data-ttu-id="19d09-118">\_aceptación de recepción de autenticación \_</span><span class="sxs-lookup"><span data-stu-id="19d09-118">AUTH\_RECV\_ACCEPT</span></span>

<span data-ttu-id="19d09-119">Un filtro en la capa de FWPM de mensajes de recepción de la autenticación Ale de la versión [**\_ \_ \_ \_ \_ Accept \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las llamadas de aceptación de TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-accept) , para los primeros paquetes UDP (unidifusión) de una tupla de puerto/dirección remota única, y para los primeros mensajes entrantes de ICMP de error (unidifusión) con un tipo, código e identificador ICMP únicos.</span><span class="sxs-lookup"><span data-stu-id="19d09-119">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) calls, for first UDP packets (unicast) from a unique remote address/port tuple, and for first inbound non-error ICMP messages (unicast) with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="19d09-120">Los protocolos que no son TCP o ICMP se tratan como UDP.</span><span class="sxs-lookup"><span data-stu-id="19d09-120">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="19d09-121">Los paquetes TCP recibidos por Sockets sin formato se controlan de forma similar al tráfico UDP.</span><span class="sxs-lookup"><span data-stu-id="19d09-121">TCP packets received by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="19d09-122">Es decir, solo se filtrarán el primer envío de TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-send) y el primer TCP [**RECV ()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre Sockets sin formato.</span><span class="sxs-lookup"><span data-stu-id="19d09-122">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="auth_connect"></a><span data-ttu-id="19d09-123">conexión de autenticación \_</span><span class="sxs-lookup"><span data-stu-id="19d09-123">AUTH\_CONNECT</span></span>

<span data-ttu-id="19d09-124">Se hace coincidir un filtro en la capa FWPM de la [**\_ \_ \_ conexión Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) de la capa de la conexión TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-connect) , para los primeros paquetes UDP enviados a una única dirección remota y a una tupla de puerto, y para los primeros mensajes salientes de ICMP que no son de error con un tipo, código e identificador de ICMP único.</span><span class="sxs-lookup"><span data-stu-id="19d09-124">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) calls, for first UDP packets sent to a unique remote address and port tuple, and for first outbound non-error ICMP messages with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="19d09-125">Los protocolos que no son TCP o ICMP se tratan como UDP.</span><span class="sxs-lookup"><span data-stu-id="19d09-125">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="19d09-126">Los paquetes TCP enviados por Sockets sin formato se controlan de forma similar al tráfico UDP.</span><span class="sxs-lookup"><span data-stu-id="19d09-126">TCP packets sent by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="19d09-127">Es decir, solo se filtrarán el primer envío de TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-send) y el primer TCP [**RECV ()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre Sockets sin formato.</span><span class="sxs-lookup"><span data-stu-id="19d09-127">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="flow_established"></a><span data-ttu-id="19d09-128">FLUJO \_ establecido</span><span class="sxs-lookup"><span data-stu-id="19d09-128">FLOW\_ESTABLISHED</span></span>

<span data-ttu-id="19d09-129">Un filtro en el [**flujo ALE de nivel FWPM establecido en la capa \_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide después de que un protocolo de enlace de tres vías TCP se haya completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="19d09-129">A filter at the [**FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after a TCP three-way handshake has successfully completed.</span></span> <span data-ttu-id="19d09-130">En el caso del tráfico que no es TCP, se hace coincidir el filtro inmediatamente después de que se cumplan los filtros de la **\_ \_ aceptación de auth** o las capas de **\_ conexión de autenticación** .</span><span class="sxs-lookup"><span data-stu-id="19d09-130">For non-TCP traffic, the filter is matched immediately after filters from **AUTH\_RECV\_ACCEPT** or **AUTH\_CONNECT** layers are matched.</span></span>

<span data-ttu-id="19d09-131">Un filtro en esta capa no debe devolver Block ni permit.</span><span class="sxs-lookup"><span data-stu-id="19d09-131">A filter at this layer should not return Block or Permit.</span></span>

<span data-ttu-id="19d09-132">Este nivel lo usan los controladores de llamada para realizar un seguimiento del estado de la conexión, que se describe en detalle en la documentación del [Kit de controladores de Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="19d09-132">This layer is used by callout drivers to track connection state, described in detail in the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) documentation.</span></span>

## <a name="resource_release"></a><span data-ttu-id="19d09-133">liberación de recursos \_</span><span class="sxs-lookup"><span data-stu-id="19d09-133">RESOURCE\_RELEASE</span></span>

<span data-ttu-id="19d09-134">Una vez que se han liberado los recursos asignados a través de la **\_ asignación de recursos** , se ha liberado un filtro en la capa de la [**\_ \_ \_ \_ versión \_ V {4 \| 6} del recurso Ale de la capa FWPM**](management-filtering-layer-identifiers-.md) .</span><span class="sxs-lookup"><span data-stu-id="19d09-134">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_RELEASE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after resources that were allocated via **RESOURCE\_ASSIGNMENT** have been freed.</span></span>

## <a name="endpoint_closure"></a><span data-ttu-id="19d09-135">cierre de extremo \_</span><span class="sxs-lookup"><span data-stu-id="19d09-135">ENDPOINT\_CLOSURE</span></span>

<span data-ttu-id="19d09-136">Un filtro en la capa de [**FWPM de \_ cierre del punto de \_ \_ conexión Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide cuando se cierra un flujo TCP o un extremo de sockets UDP conectados.</span><span class="sxs-lookup"><span data-stu-id="19d09-136">A filter at the [**FWPM\_LAYER\_ALE\_ENDPOINT\_CLOSURE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched when a connected TCP flow or UDP sockets endpoint is closed.</span></span>

## <a name="connect_redirect"></a><span data-ttu-id="19d09-137">CONECTAR \_ REdirección</span><span class="sxs-lookup"><span data-stu-id="19d09-137">CONNECT\_REDIRECT</span></span>

<span data-ttu-id="19d09-138">Un filtro en el nivel de [**FWPM de \_ \_ \_ redireccionamiento de la conexión Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) de la capa se permite modificar los puertos y las direcciones remotas.</span><span class="sxs-lookup"><span data-stu-id="19d09-138">A filter at the [**FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of remote addresses and ports.</span></span> <span data-ttu-id="19d09-139">La conexión saliente se redirigirá mientras dure la conexión.</span><span class="sxs-lookup"><span data-stu-id="19d09-139">The outbound connection will be redirected for the duration of that connection.</span></span>

## <a name="bind_redirect"></a><span data-ttu-id="19d09-140">redirección de enlace \_</span><span class="sxs-lookup"><span data-stu-id="19d09-140">BIND\_REDIRECT</span></span>

<span data-ttu-id="19d09-141">Un filtro en el nivel de [**\_ \_ \_ redirección de enlace Ale \_ \_ V {4 \| 6} de nivel FWPM**](management-filtering-layer-identifiers-.md) permite modificar la dirección local y los puertos del socket subyacente.</span><span class="sxs-lookup"><span data-stu-id="19d09-141">A filter at the [**FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of the underlying socket's local address and ports.</span></span> <span data-ttu-id="19d09-142">El socket local se redirigirá a la duración del socket</span><span class="sxs-lookup"><span data-stu-id="19d09-142">The local socket will be redirected for the lifetime of the socket</span></span>

## <a name="ale-discard-layers"></a><span data-ttu-id="19d09-143">Capas de DESCARTe de ALE</span><span class="sxs-lookup"><span data-stu-id="19d09-143">ALE DISCARD Layers</span></span>

<span data-ttu-id="19d09-144">Para cada uno de los niveles de ALE que se han descrito anteriormente, el motor de filtrado contiene una capa de descarte coincidente.</span><span class="sxs-lookup"><span data-stu-id="19d09-144">For each of the ALE layers described above the filtering engine contains a matching discard layer.</span></span> <span data-ttu-id="19d09-145">Las capas de descarte de ALE se usan en las llamadas para fines de registro.</span><span class="sxs-lookup"><span data-stu-id="19d09-145">The ALE discard layers are used by callouts for logging purposes.</span></span> <span data-ttu-id="19d09-146">Los paquetes y las indicaciones que se han descartado en uno de los niveles de filtrado ALE se indican a la capa de descarte de ALE.</span><span class="sxs-lookup"><span data-stu-id="19d09-146">Packets and indications that have been discarded at one of the ALE filtering layers are indicated to the matching ALE discard layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19d09-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19d09-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19d09-148">Aplicación del nivel de aplicación (ALE)</span><span class="sxs-lookup"><span data-stu-id="19d09-148">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="19d09-149">Filtrado con estado ALE</span><span class="sxs-lookup"><span data-stu-id="19d09-149">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="19d09-150">Tráfico de multidifusión/difusión ALE</span><span class="sxs-lookup"><span data-stu-id="19d09-150">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="19d09-151">Reautorización de ALE</span><span class="sxs-lookup"><span data-stu-id="19d09-151">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="19d09-152">Personalización del flujo ALE</span><span class="sxs-lookup"><span data-stu-id="19d09-152">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="19d09-153">Flujos de paquetes TCP</span><span class="sxs-lookup"><span data-stu-id="19d09-153">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="19d09-154">Flujos de paquetes UDP</span><span class="sxs-lookup"><span data-stu-id="19d09-154">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="19d09-155">Funciones de Winsock</span><span class="sxs-lookup"><span data-stu-id="19d09-155">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[<span data-ttu-id="19d09-156">**Marcas de condición de filtrado**</span><span class="sxs-lookup"><span data-stu-id="19d09-156">**Filtering Condition Flags**</span></span>](filtering-condition-flags-.md)
</dt> <dt>

[<span data-ttu-id="19d09-157">**Condiciones de filtrado disponibles en cada nivel de filtrado**</span><span class="sxs-lookup"><span data-stu-id="19d09-157">**Filtering Conditions Available At Each Filtering Layer**</span></span>](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 