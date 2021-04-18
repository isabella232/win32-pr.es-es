---
description: AppSequence información contenida en WS-Discovery anuncios y mensajes de respuesta (Hello, ProbeMatches y ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Reglas de validación de AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544814"
---
# <a name="appsequence-validation-rules"></a><span data-ttu-id="0f069-103">Reglas de validación de AppSequence</span><span class="sxs-lookup"><span data-stu-id="0f069-103">AppSequence Validation Rules</span></span>

<span data-ttu-id="0f069-104">AppSequence información contenida en WS-Discovery anuncios y mensajes de respuesta ([Hello](hello-message.md), [ProbeMatches](probematches-message.md)y [ResolveMatches](resolvematches-message.md)).</span><span class="sxs-lookup"><span data-stu-id="0f069-104">AppSequence information contained in WS-Discovery announcement and response messages ([Hello](hello-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md)).</span></span> <span data-ttu-id="0f069-105">WSDAPI procesa y valida esta información antes de pasar estos mensajes a los componentes situados por encima de la pila (como el explorador de red o una aplicación que llama a WSDAPI).</span><span class="sxs-lookup"><span data-stu-id="0f069-105">This information is processed and validated by WSDAPI before these messages are passed on to components above the stack (such as Network Explorer or an application calling into WSDAPI).</span></span>

<span data-ttu-id="0f069-106">En el código XML siguiente se muestra un elemento AppSequence de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0f069-106">The following XML shows a sample AppSequence element.</span></span> <span data-ttu-id="0f069-107">El prefijo WSD hace referencia al espacio de nombres `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="0f069-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

<span data-ttu-id="0f069-108">WSDAPI omite los mensajes obsoletos.</span><span class="sxs-lookup"><span data-stu-id="0f069-108">WSDAPI ignores stale messages.</span></span> <span data-ttu-id="0f069-109">Para cada dispositivo (identificado de forma exclusiva por la dirección del punto de conexión en el cuerpo de SOAP), WSDAPI omite los mensajes con un MessageNumber AppSequence inferior al último mensaje que se ha observado.</span><span class="sxs-lookup"><span data-stu-id="0f069-109">For each device (uniquely identified by the Endpoint Address in the SOAP Body), WSDAPI ignores any messages with an AppSequence MessageNumber lower than the last message seen.</span></span>

<span data-ttu-id="0f069-110">WSDAPI omite los anuncios XAddr obsoletos.</span><span class="sxs-lookup"><span data-stu-id="0f069-110">WSDAPI ignores stale XAddr announcements.</span></span> <span data-ttu-id="0f069-111">Si el InstanceId AppSequence es inferior al último InstanceId detectado, WSDAPI omite el XAddrs anunciado en el cuerpo de SOAP.</span><span class="sxs-lookup"><span data-stu-id="0f069-111">If the AppSequence InstanceId is lower than the last InstanceId seen, WSDAPI ignores the XAddrs advertised in the SOAP body.</span></span> <span data-ttu-id="0f069-112">Además, si InstanceId es el mismo que el anterior pero el MetadataVersion es inferior al último MetadataVersion, WSDAPI omite XAddrs.</span><span class="sxs-lookup"><span data-stu-id="0f069-112">Also, if the InstanceId is the same as previous but the MetadataVersion is lower than the last MetadataVersion, WSDAPI ignores the XAddrs.</span></span>

<span data-ttu-id="0f069-113">WSDAPI omite los mensajes duplicados de WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="0f069-113">WSDAPI ignores duplicate WS-Discovery messages.</span></span> <span data-ttu-id="0f069-114">Si se envían dos mensajes de WS-Discovery idénticos a WSDAPI, solo se procesará el primero recibido.</span><span class="sxs-lookup"><span data-stu-id="0f069-114">If two identical WS-Discovery messages are sent to WSDAPI, only the first received will be processed.</span></span> <span data-ttu-id="0f069-115">Normalmente solo es pertinente para las aplicaciones que llaman directamente a las interfaces [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) o [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .</span><span class="sxs-lookup"><span data-stu-id="0f069-115">This is typically only relevant for applications that call directly into the [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) or [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f069-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0f069-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f069-117">Patrones de mensajes de intercambio de metadatos y detección</span><span class="sxs-lookup"><span data-stu-id="0f069-117">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



