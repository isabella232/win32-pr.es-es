---
description: Un conjunto de herramientas de depuración basado en servicios web en la API de dispositivos (WSDAPI) está disponible en el Windows SDK y en el kit de controladores de Windows (WDK).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Herramientas de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156669"
---
# <a name="debugging-tools"></a><span data-ttu-id="69321-103">Herramientas de depuración</span><span class="sxs-lookup"><span data-stu-id="69321-103">Debugging Tools</span></span>

<span data-ttu-id="69321-104">Un conjunto de herramientas de depuración basado en servicios web en la API de dispositivos (WSDAPI) está disponible en el Windows SDK y en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="69321-104">A debugging toolset built on Web Services on Devices API (WSDAPI) is available in the Windows SDK and the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="69321-105">Estas herramientas se pueden usar para probar la funcionalidad de las aplicaciones personalizadas escritas en WSDAPI, o los dispositivos y clientes escritos con otras pilas de perfiles de dispositivo para servicios web (DPWS).</span><span class="sxs-lookup"><span data-stu-id="69321-105">These tools can be used to test the functionality of custom applications written on WSDAPI, or devices and clients written using other Device Profile for Web Services (DPWS) stacks.</span></span>

<span data-ttu-id="69321-106">Las herramientas host de depuración WSD (wsddebug \_host.exe) y cliente de depuración WSD (wsddebug \_client.exe) se pueden usar para inspeccionar las características de los clientes o hosts de DPWS.</span><span class="sxs-lookup"><span data-stu-id="69321-106">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools can be used to inspect the characteristics of DPWS clients or hosts.</span></span> <span data-ttu-id="69321-107">También se pueden usar para solucionar problemas de conectividad o configuración.</span><span class="sxs-lookup"><span data-stu-id="69321-107">They can also be used to troubleshoot connectivity or configuration problems.</span></span> <span data-ttu-id="69321-108">Para obtener más información, consulte la [Guía de solución de problemas de WSDAPI](wsdapi-troubleshooting-guide.md).</span><span class="sxs-lookup"><span data-stu-id="69321-108">For more information, see [WSDAPI Troubleshooting Guide](wsdapi-troubleshooting-guide.md).</span></span> <span data-ttu-id="69321-109">Estas herramientas solo están disponibles en el SDK de.</span><span class="sxs-lookup"><span data-stu-id="69321-109">These tools are only available in the SDK.</span></span> <span data-ttu-id="69321-110">Las herramientas del SDK se encuentran en el siguiente directorio: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="69321-110">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="69321-111">La [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) se puede usar para probar la interoperabilidad de nivel de SOAP o de transporte (es decir, garantizar que los mensajes tienen el formato correcto).</span><span class="sxs-lookup"><span data-stu-id="69321-111">The [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) can be used to test SOAP-level or transport-level interoperability (that is, ensuring messages are well-formed).</span></span> <span data-ttu-id="69321-112">Esta herramienta solo está disponible en el WDK.</span><span class="sxs-lookup"><span data-stu-id="69321-112">This tool is only available in the WDK.</span></span>

## <a name="the-wsd-debug-client"></a><span data-ttu-id="69321-113">El cliente de depuración de WSD</span><span class="sxs-lookup"><span data-stu-id="69321-113">The WSD Debug Client</span></span>

<span data-ttu-id="69321-114">El cliente de depuración de WSD (wsddebug \_client.exe) proporciona una consola interactiva que se puede usar para enviar y recibir mensajes WS-Discovery y para obtener metadatos.</span><span class="sxs-lookup"><span data-stu-id="69321-114">The WSD Debug Client (wsddebug\_client.exe) provides an interactive console that can be used to send and receive WS-Discovery messages, and to obtain metadata.</span></span> <span data-ttu-id="69321-115">También se puede utilizar para generar y consumir mensajes de multidifusión sin procesar.</span><span class="sxs-lookup"><span data-stu-id="69321-115">It can also be used to generate and consume raw multicast messages.</span></span>

<span data-ttu-id="69321-116">El cliente de depuración de WSD funciona en uno de estos tres modos: multidifusión, detección y metadatos.</span><span class="sxs-lookup"><span data-stu-id="69321-116">The WSD Debug Client operates in one of three modes: multicast, discovery, and metadata.</span></span>



| <span data-ttu-id="69321-117">Mode</span><span class="sxs-lookup"><span data-stu-id="69321-117">Mode</span></span>      | <span data-ttu-id="69321-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="69321-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69321-119">Multidifusión</span><span class="sxs-lookup"><span data-stu-id="69321-119">Multicast</span></span> | <span data-ttu-id="69321-120">En el modo de multidifusión, el cliente de depuración de WSD envía y recibe mensajes de multidifusión sin formato en el puerto UDP 3702, tal y como se define en WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="69321-120">In Multicast mode, the WSD Debug Client sends and receives unformatted multicast messages on UDP port 3702, as defined in WS-Discovery.</span></span> <span data-ttu-id="69321-121">El usuario puede guardar estos mensajes SOAP en un archivo de texto y puede modificar y redifundir los mensajes con el cliente de depuración de WSD.</span><span class="sxs-lookup"><span data-stu-id="69321-121">The user may save these SOAP messages in a text file, and may modify and rebroadcast the messages with the WSD Debug Client.</span></span>                                                                                                                                 |
| <span data-ttu-id="69321-122">de esquema JSON</span><span class="sxs-lookup"><span data-stu-id="69321-122">Discovery</span></span> | <span data-ttu-id="69321-123">En el modo de detección, el cliente de depuración de WSD envía y recibe mensajes de WS-Discovery con formato.</span><span class="sxs-lookup"><span data-stu-id="69321-123">In Discovery mode, the WSD Debug Client sends and receives formatted WS-Discovery messages.</span></span> <span data-ttu-id="69321-124">Puede mostrar los mensajes [Hello](hello-message.md), [bye](bye-message.md), [ProbeMatches](probematches-message.md)y [ResolveMatches](resolvematches-message.md) recibidos.</span><span class="sxs-lookup"><span data-stu-id="69321-124">It can display received [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md) messages.</span></span> <span data-ttu-id="69321-125">Puede enviar mensajes de [sondeo](probe-message.md) a través de UDP o http y [resolver](resolve-message.md) mensajes a través de UDP.</span><span class="sxs-lookup"><span data-stu-id="69321-125">It can send [Probe](probe-message.md) messages over UDP or HTTP, and [Resolve](resolve-message.md) messages over UDP.</span></span> |
| <span data-ttu-id="69321-126">Metadatos</span><span class="sxs-lookup"><span data-stu-id="69321-126">Metadata</span></span>  | <span data-ttu-id="69321-127">Además de implementar todas las características del modo de detección, el modo de metadatos también intenta recuperar los metadatos de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="69321-127">In addition to implementing all of the features of Discovery mode, Metadata mode also attempts to retrieve metadata from devices.</span></span>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="69321-128">Para obtener más información, vea [usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md) [mediante un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md)y el [uso del cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="69321-128">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md), and [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

## <a name="the-wsd-debug-host"></a><span data-ttu-id="69321-129">Host de depuración de WSD</span><span class="sxs-lookup"><span data-stu-id="69321-129">The WSD Debug Host</span></span>

<span data-ttu-id="69321-130">El host de depuración de WSD (wsddebug \_host.exe) proporciona una consola interactiva que se usa para anunciar el host, responder a las solicitudes de cliente e imprimir información de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="69321-130">The WSD Debug Host (wsddebug\_host.exe) provides an interactive console used to announce the host, respond to client requests, and print diagnostic information.</span></span>

<span data-ttu-id="69321-131">El host de depuración de WSD funciona en uno de los dos modos siguientes: detección y metadatos.</span><span class="sxs-lookup"><span data-stu-id="69321-131">The WSD Debug Host operates in one of two modes: discovery and metadata.</span></span>



| <span data-ttu-id="69321-132">Mode</span><span class="sxs-lookup"><span data-stu-id="69321-132">Mode</span></span>      | <span data-ttu-id="69321-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="69321-133">Description</span></span>                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69321-134">de esquema JSON</span><span class="sxs-lookup"><span data-stu-id="69321-134">Discovery</span></span> | <span data-ttu-id="69321-135">En el modo de detección, el host de depuración de WSD imprime los mensajes de WS-Discovery con formato.</span><span class="sxs-lookup"><span data-stu-id="69321-135">In Discovery mode, the WSD Debug Host prints formatted WS-Discovery messages.</span></span> <span data-ttu-id="69321-136">También envía mensajes [Hello](hello-message.md) y [bye](bye-message.md) , y responde automáticamente a los mensajes de [sondeo](probe-message.md) y [resolución](resolve-message.md) .</span><span class="sxs-lookup"><span data-stu-id="69321-136">It also sends [Hello](hello-message.md) and [Bye](bye-message.md) messages, and automatically responds to [Probe](probe-message.md) and [Resolve](resolve-message.md) messages.</span></span> |
| <span data-ttu-id="69321-137">Metadatos</span><span class="sxs-lookup"><span data-stu-id="69321-137">Metadata</span></span>  | <span data-ttu-id="69321-138">Además de implementar todas las características del modo de detección, el modo de metadatos anuncia un servicio de metadatos y permite que los clientes se conecten y realicen el intercambio de metadatos.</span><span class="sxs-lookup"><span data-stu-id="69321-138">In addition to implementing all of the features of Discovery mode, Metadata mode advertises a metadata service and allows clients to connect and perform metadata exchange.</span></span>                                                                                       |



 

<span data-ttu-id="69321-139">Para obtener más información, vea [usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md) y [usar un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="69321-139">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) and [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69321-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69321-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69321-141">Desarrollo de aplicaciones WSD en Windows</span><span class="sxs-lookup"><span data-stu-id="69321-141">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="69321-142">Herramientas de desarrollo de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="69321-142">WSDAPI Development Tools</span></span>](wsdapi-development-tools.md)
</dt> <dt>

[<span data-ttu-id="69321-143">Guía de solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="69321-143">WSDAPI Troubleshooting Guide</span></span>](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



