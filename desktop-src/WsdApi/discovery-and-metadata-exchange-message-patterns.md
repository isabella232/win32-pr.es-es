---
description: Los clientes y los hosts de los servicios web (DPWS) se comunican a través de la red mediante una serie de mensajes SOAP a través de UDP y HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Patrones de mensajes de intercambio de metadatos y detección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104279758"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a><span data-ttu-id="1d9f4-103">Patrones de mensajes de intercambio de metadatos y detección</span><span class="sxs-lookup"><span data-stu-id="1d9f4-103">Discovery and Metadata Exchange Message Patterns</span></span>

<span data-ttu-id="1d9f4-104">Los clientes y los hosts de los servicios web (DPWS) se comunican a través de la red mediante una serie de mensajes SOAP a través de UDP y HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-104">Device Profile for Web Services (DPWS) hosts and clients communicate over the network using a series of SOAP messages over UDP and HTTP.</span></span>

<span data-ttu-id="1d9f4-105">En el diagrama siguiente se muestra información general sobre el tráfico UDP y HTTP esperado entre un host y un cliente de DPWS.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-105">The following diagram shows an overview of the expected UDP and HTTP traffic between a DPWS host and client.</span></span>

![Diagrama que muestra el tráfico UDP y HTTP entre un host y un cliente de DPWS.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

<span data-ttu-id="1d9f4-107">Los mensajes [Hello](hello-message.md), [bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md)y [Get](get--metadata-exchange--http-request-and-message.md) se generan sin la solicitud de red; Estos mensajes se utilizan para anunciar el estado del dispositivo o para emitir una solicitud de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-107">[Hello](hello-message.md), [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md), and [Get](get--metadata-exchange--http-request-and-message.md) messages are all generated without network solicitation; these messages are used to announce device state or to issue a search request.</span></span> <span data-ttu-id="1d9f4-108">Los mensajes [ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md)y [GetResponse](getresponse--metadata-exchange--message.md) se generan como respuesta a sondeo, resolución y obtención de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-108">[ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md), and [GetResponse](getresponse--metadata-exchange--message.md) messages are generated in response to Probe, Resolve and Get messages.</span></span>

<span data-ttu-id="1d9f4-109">Los mensajes [Hello](hello-message.md), [bye](bye-message.md), [Resolve](resolve-message.md)y [ResolveMatches](resolvematches-message.md) siempre se producirán a través de UDP.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-109">[Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md), and [ResolveMatches](resolvematches-message.md) messages will always occur over UDP.</span></span> <span data-ttu-id="1d9f4-110">Del mismo modo, los mensajes de metadatos [Get](get--metadata-exchange--http-request-and-message.md) y [GetResponse](getresponse--metadata-exchange--message.md) siempre se producirán a través de http o https.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-110">Similarly, [Get](get--metadata-exchange--http-request-and-message.md) and [GetResponse](getresponse--metadata-exchange--message.md) metadata messages will always occur over HTTP or HTTPS.</span></span> <span data-ttu-id="1d9f4-111">Los mensajes de [sondeo](probe-message.md) y [ProbeMatches](probematches-message.md) se transmiten normalmente a través de UDP, pero tienen lugar a través de una conexión http o https en un escenario de detección dirigido.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-111">[Probe](probe-message.md) and [ProbeMatches](probematches-message.md) messages are normally transmitted over UDP, but take place over an HTTP or HTTPS connection in a directed discovery scenario.</span></span> <span data-ttu-id="1d9f4-112">Para obtener más información sobre los patrones de mensajes de detección dirigidos, consulte [solución de problemas de aplicaciones mediante la detección dirigida](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="1d9f4-112">For more information about directed discovery message patterns, see [Troubleshooting Applications Using Directed Discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="1d9f4-113">En la siguiente lista se muestra la secuencia típica de mensajes en la conexión.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-113">The following list shows the typical sequence of messages on the wire.</span></span> <span data-ttu-id="1d9f4-114">No todos los mensajes son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-114">Not all messages are mandatory.</span></span>

1.  [<span data-ttu-id="1d9f4-115">Hola</span><span class="sxs-lookup"><span data-stu-id="1d9f4-115">Hello</span></span>](hello-message.md)
2.  [<span data-ttu-id="1d9f4-116">Sondeo</span><span class="sxs-lookup"><span data-stu-id="1d9f4-116">Probe</span></span>](probe-message.md)
3.  [<span data-ttu-id="1d9f4-117">ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="1d9f4-117">ProbeMatches</span></span>](probematches-message.md)
4.  [<span data-ttu-id="1d9f4-118">Resolver</span><span class="sxs-lookup"><span data-stu-id="1d9f4-118">Resolve</span></span>](resolve-message.md)
5.  [<span data-ttu-id="1d9f4-119">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="1d9f4-119">ResolveMatches</span></span>](resolvematches-message.md)
6.  <span data-ttu-id="1d9f4-120">[Get](get--metadata-exchange--http-request-and-message.md) (solicitud de intercambio de metadatos)</span><span class="sxs-lookup"><span data-stu-id="1d9f4-120">[Get](get--metadata-exchange--http-request-and-message.md) (metadata exchange request)</span></span>
7.  [<span data-ttu-id="1d9f4-121">GetResponse</span><span class="sxs-lookup"><span data-stu-id="1d9f4-121">GetResponse</span></span>](getresponse--metadata-exchange--message.md)
8.  [<span data-ttu-id="1d9f4-122">Adiós</span><span class="sxs-lookup"><span data-stu-id="1d9f4-122">Bye</span></span>](bye-message.md)

## <a name="related-topics"></a><span data-ttu-id="1d9f4-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d9f4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d9f4-124">Acerca de los servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="1d9f4-124">About Web Services on Devices</span></span>](about-web-services-for-devices.md)
</dt> </dl>

 

 



