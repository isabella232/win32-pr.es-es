---
description: Enumera los procedimientos de diagnóstico que se deben usar al solucionar problemas de clientes de detección de funciones.
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Solución de problemas de clientes de detección de funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811401"
---
# <a name="troubleshooting-function-discovery-clients"></a><span data-ttu-id="266e8-103">Solución de problemas de clientes de detección de funciones</span><span class="sxs-lookup"><span data-stu-id="266e8-103">Troubleshooting Function Discovery Clients</span></span>

<span data-ttu-id="266e8-104">Clientes de detección de funciones:</span><span class="sxs-lookup"><span data-stu-id="266e8-104">Function Discovery clients:</span></span>

-   <span data-ttu-id="266e8-105">Usar siempre WS-Discovery UDP para la detección de dispositivos</span><span class="sxs-lookup"><span data-stu-id="266e8-105">Always use UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="266e8-106">Iniciar siempre conexiones HTTP o HTTPS para el intercambio de metadatos</span><span class="sxs-lookup"><span data-stu-id="266e8-106">Always initiate HTTP or HTTPS connections for metadata exchange</span></span>
-   <span data-ttu-id="266e8-107">A veces, usar el descubrimiento dirigido</span><span class="sxs-lookup"><span data-stu-id="266e8-107">Sometimes use directed discovery</span></span>
-   <span data-ttu-id="266e8-108">A veces, se usa un canal seguro (HTTPS) para el intercambio de metadatos</span><span class="sxs-lookup"><span data-stu-id="266e8-108">Sometimes use a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="266e8-109">En la siguiente lista se muestra la secuencia típica de mensajes enviados y recibidos por los clientes de detección de funciones.</span><span class="sxs-lookup"><span data-stu-id="266e8-109">The following list shows the typical sequence of messages sent and received by Function Discovery clients.</span></span> <span data-ttu-id="266e8-110">No todos los mensajes son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="266e8-110">Not all messages are mandatory.</span></span>

1.  <span data-ttu-id="266e8-111">El cliente envía un mensaje de [sondeo](probe-message.md) para detectar dispositivos y servicios.</span><span class="sxs-lookup"><span data-stu-id="266e8-111">The client sends a [Probe](probe-message.md) message to discover devices and services.</span></span> <span data-ttu-id="266e8-112">Si el cliente usa la detección dirigida, este mensaje se envía a través de HTTP o HTTPS. de lo contrario, el mensaje se envía mediante multidifusión de UDP al puerto 3702.</span><span class="sxs-lookup"><span data-stu-id="266e8-112">If the client is using directed discovery then this message is sent over HTTP or HTTPS; otherwise, the message is sent by UDP multicast to port 3702.</span></span>
2.  <span data-ttu-id="266e8-113">El cliente recibe mensajes [ProbeMatches](probematches-message.md) de dispositivos o servicios coincidentes.</span><span class="sxs-lookup"><span data-stu-id="266e8-113">The client receives [ProbeMatches](probematches-message.md) messages from matching devices or services.</span></span> <span data-ttu-id="266e8-114">Los mensajes de detección dirigidos se envían a través de HTTP o HTTPS. de lo contrario, los mensajes se envían por unidifusión UDP y se originan desde el puerto 3702.</span><span class="sxs-lookup"><span data-stu-id="266e8-114">Directed discovery messages are sent over HTTP or HTTPS; otherwise, these messages are sent by UDP unicast and originate from port 3702.</span></span>
3.  <span data-ttu-id="266e8-115">Si no se incluyó ningún XAddrs en el mensaje ProbeMatches, el cliente enviará un mensaje de [resolución](resolve-message.md) mediante multidifusión UDP al puerto 3702.</span><span class="sxs-lookup"><span data-stu-id="266e8-115">If no XAddrs were included in the ProbeMatches message, then the client will send a [Resolve](resolve-message.md) message by UDP multicast to port 3702.</span></span>
4.  <span data-ttu-id="266e8-116">Si se ha enviado un mensaje de [resolución](resolve-message.md) , el cliente recibe un mensaje [ResolveMatches](resolvematches-message.md) de los servicios coincidentes.</span><span class="sxs-lookup"><span data-stu-id="266e8-116">If a [Resolve](resolve-message.md) message was sent, then the client receives a [ResolveMatches](resolvematches-message.md) message from matching services.</span></span> <span data-ttu-id="266e8-117">Este mensaje lo envía la unidifusión UDP desde el puerto 3702 al puerto en el que se originó el mensaje de resolución.</span><span class="sxs-lookup"><span data-stu-id="266e8-117">This message is sent by UDP unicast from port 3702 to the port where the Resolve message originated.</span></span>
5.  <span data-ttu-id="266e8-118">El cliente envía un mensaje [Get](get--metadata-exchange--http-request-and-message.md) para solicitar los metadatos del dispositivo o servicio.</span><span class="sxs-lookup"><span data-stu-id="266e8-118">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to request metadata from the device or service.</span></span> <span data-ttu-id="266e8-119">HTTP o HTTPS envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="266e8-119">This message is sent by HTTP or HTTPS.</span></span>
6.  <span data-ttu-id="266e8-120">El cliente recibe un mensaje [GetResponse](getresponse--metadata-exchange--message.md) con los metadatos del dispositivo o servicio.</span><span class="sxs-lookup"><span data-stu-id="266e8-120">The client receives a [GetResponse](getresponse--metadata-exchange--message.md) message with the device or service metadata.</span></span> <span data-ttu-id="266e8-121">HTTP o HTTPS envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="266e8-121">This message is sent by HTTP or HTTPS.</span></span>

<span data-ttu-id="266e8-122">Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con un cliente de detección de funciones.</span><span class="sxs-lookup"><span data-stu-id="266e8-122">The following diagnostic procedures should be used (in order) to help identify problems with a Function Discovery client.</span></span>

<span data-ttu-id="266e8-123">**Para solucionar problemas de un cliente de detección de funciones**</span><span class="sxs-lookup"><span data-stu-id="266e8-123">**To troubleshoot a Function Discovery client**</span></span>

1.  <span data-ttu-id="266e8-124">Si se usa la detección dirigida, [solucione los problemas de detección dirigida](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="266e8-124">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="266e8-125">[Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="266e8-125">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="266e8-126">[Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="266e8-126">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="266e8-127">[Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="266e8-127">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="266e8-128">[Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="266e8-128">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="266e8-129">[Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="266e8-129">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="266e8-130">[Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="266e8-130">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="266e8-131">[Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="266e8-131">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="266e8-132">Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="266e8-132">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="266e8-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="266e8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="266e8-134">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="266e8-134">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



