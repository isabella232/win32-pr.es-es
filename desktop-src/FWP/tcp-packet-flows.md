---
title: Flujos de paquetes TCP
description: El orden en que se recorren las capas del motor de filtro de la plataforma de filtrado de Windows (WFP) durante una sesión TCP típica.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994399"
---
# <a name="tcp-packet-flows"></a><span data-ttu-id="a708b-103">Flujos de paquetes TCP</span><span class="sxs-lookup"><span data-stu-id="a708b-103">TCP Packet Flows</span></span>

<span data-ttu-id="a708b-104">En esta sección se describe el orden en el que se recorren las capas del motor de filtro de la plataforma de filtrado de Windows (WFP) durante una sesión TCP típica.</span><span class="sxs-lookup"><span data-stu-id="a708b-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical TCP session.</span></span>

> [!Note]  
> <span data-ttu-id="a708b-105">Los flujos de paquetes TCP para IPv6 siguen el mismo patrón que para IPv4.</span><span class="sxs-lookup"><span data-stu-id="a708b-105">TCP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="a708b-106">Los flujos de paquetes que no son TCP siguen el mismo patrón que los [flujos de paquetes UDP](udp-packet-flows.md).</span><span class="sxs-lookup"><span data-stu-id="a708b-106">Non-TCP packet flows follow the same pattern as [UDP packet flows](udp-packet-flows.md).</span></span>

 

## <a name="tcp-connection-establishment"></a><span data-ttu-id="a708b-107">Establecimiento de la conexión TCP</span><span class="sxs-lookup"><span data-stu-id="a708b-107">TCP Connection Establishment</span></span>

<dl> <span data-ttu-id="a708b-108">El servidor (receptor) realiza un abierto pasivo</span><span class="sxs-lookup"><span data-stu-id="a708b-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="a708b-109">enlace: \_ \_ redirección de enlace Ale V4 de nivel FWPM \_ \_ \_ (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="a708b-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="a708b-110">BIND: \_ asignación de \_ \_ recursos Ale \_ \_ V4 de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="a708b-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="a708b-111">Listen: FWPM de la \_ autenticación Ale de capa de la \_ \_ \_ escucha \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-111">listen: FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V4</span></span>

  
<span data-ttu-id="a708b-112">El cliente (remitente) realiza una apertura activa</span><span class="sxs-lookup"><span data-stu-id="a708b-112">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="a708b-113">enlace: \_ \_ redirección de enlace Ale V4 de nivel FWPM \_ \_ \_ (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="a708b-113">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="a708b-114">BIND: \_ asignación de \_ \_ recursos Ale \_ \_ V4 de capa FWPM</span><span class="sxs-lookup"><span data-stu-id="a708b-114">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="a708b-115">Connect: \_ REdireccionamiento de la FWPM del nivel de \_ \_ conexión Ale \_ \_ V4 (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="a708b-115">connect: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="a708b-116">conexión: FWPM \_ capa \_ de \_ autenticación \_ Ale \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-116">connect: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="a708b-117">SYN: \_ transporte de salida de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-117">SYN: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-118">SYN: FWPM de \_ nivel \_ saliente \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-118">SYN: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="a708b-119">Servidor</span><span class="sxs-lookup"><span data-stu-id="a708b-119">Server</span></span>

-   <span data-ttu-id="a708b-120">SYN: FWPM \_ Layer \_ entrante \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-120">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="a708b-121">SYN: \_ transporte de entrada de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-121">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-122">SYN: FWPM \_ capa \_ de \_ autenticación Ale de \_ recepción \_ aceptación \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-122">SYN: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="a708b-123">SYN-ACK: \_ transporte de salida de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-123">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-124">SYN-ACK: FWPM de \_ salida de nivel de \_ \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-124">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="a708b-125">Remoto</span><span class="sxs-lookup"><span data-stu-id="a708b-125">Client</span></span>

-   <span data-ttu-id="a708b-126">SYN-ACK: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-126">SYN-ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="a708b-127">SYN-ACK: \_ transporte entrante de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-127">SYN-ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-128">\_Flujo ALE de capa de FWPM \_ \_ \_ establecido \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-128">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="a708b-129">CONFIRMACIÓN: transporte de salida de capa de FWPM \_ \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-129">ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-130">ACK: FWPM de \_ salida de nivel de \_ \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-130">ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="a708b-131">Servidor</span><span class="sxs-lookup"><span data-stu-id="a708b-131">Server</span></span>

-   <span data-ttu-id="a708b-132">ACK: FWPM de \_ entrada de nivel de \_ \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-132">ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="a708b-133">ACK: \_ transporte de entrada de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-133">ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-134">\_Flujo ALE de capa de FWPM \_ \_ \_ establecido \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-134">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="a708b-135">Se completa la escucha.</span><span class="sxs-lookup"><span data-stu-id="a708b-135">Listen completes.</span></span> <span data-ttu-id="a708b-136">El servidor puede realizar una aceptación.</span><span class="sxs-lookup"><span data-stu-id="a708b-136">Server can perform an accept.</span></span>

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="a708b-137">TCP SYN recibidos sin una escucha en el puerto o protocolo</span><span class="sxs-lookup"><span data-stu-id="a708b-137">TCP SYN Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="a708b-138">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="a708b-138">Server (receiver)</span></span>

-   <span data-ttu-id="a708b-139">SYN: FWPM \_ Layer \_ entrante \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-139">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="a708b-140">SYN: FWPM \_ capa de \_ entrada de \_ transporte \_ V4 \_ descartado</span><span class="sxs-lookup"><span data-stu-id="a708b-140">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4\_DISCARD</span></span>
-   <span data-ttu-id="a708b-141">RST: \_ transporte de salida de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-141">RST: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-142">RST: FWPM \_ de \_ salida de capa saliente \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-142">RST: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="a708b-143">TCP SYN sin extremo se indica en TRANSPORT discard con una condición de error específica.</span><span class="sxs-lookup"><span data-stu-id="a708b-143">TCP SYN with no endpoint is indicated at TRANSPORT discard with a specific error condition.</span></span> <span data-ttu-id="a708b-144">Bloquear este paquete en el transporte descartado para hacer que la pila no envíe el evento correspondiente (RST).</span><span class="sxs-lookup"><span data-stu-id="a708b-144">Block this packet at TRANSPORT discard to cause the stack not to send the corresponding event (RST).</span></span> <span data-ttu-id="a708b-145">Para obtener un ejemplo de filtrado de modo oculto, consulte [impedir el examen de puertos](preventing-port-scanning.md).</span><span class="sxs-lookup"><span data-stu-id="a708b-145">For an example of stealth-mode filtering, see [Preventing Port Scanning](preventing-port-scanning.md).</span></span>

 

## <a name="data-transmitted-over-a-tcp-connection"></a><span data-ttu-id="a708b-146">Datos transmitidos a través de una conexión TCP</span><span class="sxs-lookup"><span data-stu-id="a708b-146">Data Transmitted Over a TCP Connection</span></span>

<dl> <span data-ttu-id="a708b-147">Cliente (remitente)</span><span class="sxs-lookup"><span data-stu-id="a708b-147">Client (sender)</span></span>

-   <span data-ttu-id="a708b-148">Enviar</span><span class="sxs-lookup"><span data-stu-id="a708b-148">send</span></span>
-   <span data-ttu-id="a708b-149">datos: \_ flujo de capa FWPM \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-149">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="a708b-150">Segmentos TCP: \_ transporte de salida de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-150">TCP segments: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-151">Datagramas IP: FWPM \_ de \_ salida de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-151">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="a708b-152">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="a708b-152">Server (receiver)</span></span>

-   <span data-ttu-id="a708b-153">Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-153">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="a708b-154">Segmentos TCP: \_ transporte de entrada de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-154">TCP segments: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-155">datos: \_ flujo de capa FWPM \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-155">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="a708b-156">Los datos están disponibles para leer.</span><span class="sxs-lookup"><span data-stu-id="a708b-156">Data is available to read.</span></span>

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="a708b-157">Reautorización correcta de un paquete TCP</span><span class="sxs-lookup"><span data-stu-id="a708b-157">Successful Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="a708b-158">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="a708b-158">Server (receiver)</span></span>

-   <span data-ttu-id="a708b-159">Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-159">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="a708b-160">Segmento TCP: \_ transporte entrante de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-160">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-161">Segmento TCP: aceptación de autenticación Ale de FWPM de capa de la \_ \_ \_ \_ recepción \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-161">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="a708b-162">datos: \_ flujo de capa FWPM \_ \_ V4 (entrante)</span><span class="sxs-lookup"><span data-stu-id="a708b-162">data: FWPM\_LAYER\_STREAM\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="a708b-163">No se pudo reautorizar un paquete TCP</span><span class="sxs-lookup"><span data-stu-id="a708b-163">Failed Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="a708b-164">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="a708b-164">Server (receiver)</span></span>

-   <span data-ttu-id="a708b-165">Datagramas IP: FWPM \_ de \_ entrada de nivel \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-165">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="a708b-166">Segmento TCP: \_ transporte entrante de capa FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-166">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="a708b-167">Segmento TCP: aceptación de autenticación Ale de FWPM de capa de la \_ \_ \_ \_ recepción \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="a708b-167">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="a708b-168">Segmento TCP: recepción de autenticación Ale de FWPM de \_ nivel de \_ \_ \_ recepción \_ aceptación \_ V4 \_ descartada</span><span class="sxs-lookup"><span data-stu-id="a708b-168">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="tcp-connection-termination"></a><span data-ttu-id="a708b-169">Terminación de la conexión TCP</span><span class="sxs-lookup"><span data-stu-id="a708b-169">TCP Connection Termination</span></span>

<span data-ttu-id="a708b-170">La terminación de la conexión TCP no se indica en ninguna capa WFP.</span><span class="sxs-lookup"><span data-stu-id="a708b-170">TCP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a708b-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a708b-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a708b-172">Reautorización de ALE</span><span class="sxs-lookup"><span data-stu-id="a708b-172">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="a708b-173">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="a708b-173">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




