---
title: Flujos de paquetes UDP
description: El orden en que se recorren las capas del motor de filtro de la plataforma de filtrado de Windows (WFP) durante una sesión UDP típica.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357430"
---
# <a name="udp-packet-flows"></a><span data-ttu-id="8afa5-103">Flujos de paquetes UDP</span><span class="sxs-lookup"><span data-stu-id="8afa5-103">UDP Packet Flows</span></span>

<span data-ttu-id="8afa5-104">En esta sección se describe el orden en el que se recorren las capas del motor de filtro de la plataforma de filtrado de Windows (WFP) durante una sesión UDP típica.</span><span class="sxs-lookup"><span data-stu-id="8afa5-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical UDP session.</span></span>

> [!Note]  
> <span data-ttu-id="8afa5-105">Los flujos de paquetes UDP para IPv6 siguen el mismo patrón que para IPv4.</span><span class="sxs-lookup"><span data-stu-id="8afa5-105">UDP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="8afa5-106">Todos los flujos de paquetes que no son TCP siguen el mismo patrón que los flujos de paquetes UDP.</span><span class="sxs-lookup"><span data-stu-id="8afa5-106">All non-TCP packet flows follow the same pattern as UDP packet flows.</span></span>

 

## <a name="udp-connection-establishment"></a><span data-ttu-id="8afa5-107">Establecimiento de conexiones UDP</span><span class="sxs-lookup"><span data-stu-id="8afa5-107">UDP Connection Establishment</span></span>

<dl> <span data-ttu-id="8afa5-108">El servidor (receptor) realiza un abierto pasivo</span><span class="sxs-lookup"><span data-stu-id="8afa5-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="8afa5-109">enlace: \_ \_ redirección de enlace Ale V4 de nivel FWPM \_ \_ \_ (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="8afa5-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="8afa5-110">BIND: \_ asignación de \_ \_ recursos Ale \_ \_ V4 de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="8afa5-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>

  
<span data-ttu-id="8afa5-111">El cliente (remitente) realiza una apertura activa</span><span class="sxs-lookup"><span data-stu-id="8afa5-111">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="8afa5-112">enlace: \_ \_ redirección de enlace Ale V4 de nivel FWPM \_ \_ \_ (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="8afa5-112">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="8afa5-113">BIND: \_ asignación de \_ \_ recursos Ale \_ \_ V4 de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="8afa5-113">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="8afa5-114">SendTo: FWPM \_ capa \_ de \_ conexión Ale \_ V4 de redirección \_ V4 (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="8afa5-114">sendto: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="8afa5-115">SendTo: FWPM \_ capa \_ de \_ autenticación \_ Ale \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-115">sendto: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="8afa5-116">\_Flujo ALE de capa de FWPM \_ \_ \_ establecido \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-116">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="8afa5-117">datos: \_ datos de \_ datagramas de nivel FWPM \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-117">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>
-   <span data-ttu-id="8afa5-118">Mensaje UDP: \_ transporte de salida de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-118">UDP message: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="8afa5-119">Datagramas IP: FWPM \_ de \_ salida de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-119">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="8afa5-120">Servidor</span><span class="sxs-lookup"><span data-stu-id="8afa5-120">Server</span></span>

-   <span data-ttu-id="8afa5-121">Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-121">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="8afa5-122">Mensaje UDP: \_ transporte entrante de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-122">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="8afa5-123">Mensaje UDP: \_ recepción de \_ \_ autenticación Ale \_ \_ de FWPM \_</span><span class="sxs-lookup"><span data-stu-id="8afa5-123">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="8afa5-124">\_Flujo ALE de capa de FWPM \_ \_ \_ establecido \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-124">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="8afa5-125">datos: \_ datos de \_ datagramas de nivel FWPM \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-125">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="8afa5-126">Se recibió un mensaje UDP que no está escuchando en el puerto o protocolo</span><span class="sxs-lookup"><span data-stu-id="8afa5-126">UDP Message Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="8afa5-127">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="8afa5-127">Server (receiver)</span></span>

-   <span data-ttu-id="8afa5-128">Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-128">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="8afa5-129">Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4 \_</span><span class="sxs-lookup"><span data-stu-id="8afa5-129">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4\_DISCARD</span></span>
-   <span data-ttu-id="8afa5-130">Destino ICMP inaccesible: error de \_ ICMP saliente de nivel FWPM \_ \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-130">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V4</span></span>
-   <span data-ttu-id="8afa5-131">Destino ICMP inaccesible: transporte de \_ salida de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-131">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="8afa5-132">No se puede tener acceso al destino ICMP: FWPM de \_ salida de nivel \_ \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-132">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="8afa5-133">UDP sin punto de conexión se indica en IPPACKET discard con una condición de error específica.</span><span class="sxs-lookup"><span data-stu-id="8afa5-133">UDP with no endpoint is indicated at IPPACKET discard with a specific error condition.</span></span> <span data-ttu-id="8afa5-134">Bloquee este paquete en IPPACKET discard para que la pila no envíe el evento correspondiente (error de ICMP).</span><span class="sxs-lookup"><span data-stu-id="8afa5-134">Block this packet at IPPACKET discard to cause the stack not to send the corresponding event (ICMP error).</span></span>

 

## <a name="successful-reauthorization-of-a-udp-packet"></a><span data-ttu-id="8afa5-135">Reautorización correcta de un paquete UDP</span><span class="sxs-lookup"><span data-stu-id="8afa5-135">Successful Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="8afa5-136">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="8afa5-136">Server (receiver)</span></span>

-   <span data-ttu-id="8afa5-137">Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-137">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="8afa5-138">Mensaje UDP: \_ transporte entrante de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-138">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="8afa5-139">Mensaje UDP: \_ recepción de \_ \_ autenticación Ale \_ \_ de FWPM \_</span><span class="sxs-lookup"><span data-stu-id="8afa5-139">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="8afa5-140">Mensaje UDP: \_ datos de datagrama de nivel FWPM \_ \_ \_ V4 (entrante)</span><span class="sxs-lookup"><span data-stu-id="8afa5-140">UDP message: FWPM\_LAYER\_DATAGRAM\_DATA\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-udp-packet"></a><span data-ttu-id="8afa5-141">No se pudo reautorizar un paquete UDP</span><span class="sxs-lookup"><span data-stu-id="8afa5-141">Failed Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="8afa5-142">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="8afa5-142">Server (receiver)</span></span>

-   <span data-ttu-id="8afa5-143">Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-143">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="8afa5-144">Mensaje UDP: \_ transporte entrante de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="8afa5-144">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="8afa5-145">Mensaje UDP: \_ recepción de \_ \_ autenticación Ale \_ \_ de FWPM \_</span><span class="sxs-lookup"><span data-stu-id="8afa5-145">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="8afa5-146">Mensaje UDP: recepción de autenticación Ale de FWPM de \_ nivel de \_ \_ \_ recepción \_ aceptación \_ V4 \_ descartada</span><span class="sxs-lookup"><span data-stu-id="8afa5-146">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="udp-connection-termination"></a><span data-ttu-id="8afa5-147">Terminación de la conexión UDP</span><span class="sxs-lookup"><span data-stu-id="8afa5-147">UDP Connection Termination</span></span>

<span data-ttu-id="8afa5-148">La terminación de la conexión UDP no se indica en ninguna capa WFP.</span><span class="sxs-lookup"><span data-stu-id="8afa5-148">UDP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8afa5-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8afa5-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8afa5-150">Reautorización de ALE</span><span class="sxs-lookup"><span data-stu-id="8afa5-150">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="8afa5-151">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="8afa5-151">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




