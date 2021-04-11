---
description: Las direcciones de transporte (XAddrs) incluidas en los mensajes ProbeMatches y ResolveMatches están sujetas a la validación básica antes de que WSDAPI envíe un mensaje HTTP, como una solicitud de metadatos.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Reglas de validación de XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276109"
---
# <a name="xaddr-validation-rules"></a><span data-ttu-id="04b52-103">Reglas de validación de XAddr</span><span class="sxs-lookup"><span data-stu-id="04b52-103">XAddr Validation Rules</span></span>

<span data-ttu-id="04b52-104">Las direcciones de transporte (XAddrs) incluidas en los mensajes [ProbeMatches](probematches-message.md) y [ResolveMatches](resolvematches-message.md) están sujetas a la validación básica antes de que WSDAPI envíe un mensaje http, como una solicitud de metadatos.</span><span class="sxs-lookup"><span data-stu-id="04b52-104">Transport addresses (XAddrs) included in [ProbeMatches](probematches-message.md) and [ResolveMatches](resolvematches-message.md) messages are subject to basic validation before WSDAPI sends an HTTP message, such as a metadata request.</span></span>

<span data-ttu-id="04b52-105">Para asegurarse de que los XAddrs están en la misma subred que el cliente.</span><span class="sxs-lookup"><span data-stu-id="04b52-105">This is in order to ensure that the XAddrs are on the same subnet as the client.</span></span>

<span data-ttu-id="04b52-106">En el código XML siguiente se muestra un elemento XAddrs de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="04b52-106">The following XML shows a sample XAddrs element.</span></span> <span data-ttu-id="04b52-107">El prefijo WSD hace referencia al espacio de nombres `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="04b52-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

<span data-ttu-id="04b52-108">Se deben cumplir todas las condiciones siguientes antes de que el mensaje HTTP salga de la conexión.</span><span class="sxs-lookup"><span data-stu-id="04b52-108">All of the following conditions must be met before the HTTP message will go out over the wire.</span></span>

-   <span data-ttu-id="04b52-109">XAddrs debe ser una dirección HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="04b52-109">XAddrs must be HTTP or HTTPS addresses.</span></span> <span data-ttu-id="04b52-110">XAddrs de otros esquemas se omiten.</span><span class="sxs-lookup"><span data-stu-id="04b52-110">XAddrs of other schemes are ignored.</span></span>
-   <span data-ttu-id="04b52-111">Si hay algún XAddrs HTTPS presente, todos los XAddrs deben ser HTTPS.</span><span class="sxs-lookup"><span data-stu-id="04b52-111">If any HTTPS XAddrs are present, all XAddrs must be HTTPS.</span></span> <span data-ttu-id="04b52-112">Las secciones XAddr que incluyen direcciones HTTP y HTTPS se omiten por completo.</span><span class="sxs-lookup"><span data-stu-id="04b52-112">XAddr sections which include both HTTP and HTTPS addresses are completely ignored.</span></span> <span data-ttu-id="04b52-113">Además, la dirección del punto de conexión del dispositivo debe coincidir exactamente con el XAddrs HTTPS.</span><span class="sxs-lookup"><span data-stu-id="04b52-113">Additionally, the device's endpoint address must match the HTTPS XAddrs exactly.</span></span>
-   <span data-ttu-id="04b52-114">XAddrs debe ser direcciones IP o nombres de host que puedan resolverse a través de DNS.</span><span class="sxs-lookup"><span data-stu-id="04b52-114">XAddrs must be IP addresses or hostnames resolvable through DNS.</span></span> <span data-ttu-id="04b52-115">Normalmente, se usan direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="04b52-115">Usually, IP addresses are used.</span></span>
-   <span data-ttu-id="04b52-116">Al menos una dirección IP incluida en la XAddrs (o la dirección IP resuelta desde un nombre de host incluido en XAddrs) debe estar en la misma subred que el adaptador en el que se recibió el mensaje [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="04b52-116">At least one IP address included in the XAddrs (or IP address resolved from a hostname included in the XAddrs) must be on the same subnet as the adapter over which the [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message was received.</span></span>
-   <span data-ttu-id="04b52-117">La dirección y el puerto especificados en el primer XAddr deben ser accesibles.</span><span class="sxs-lookup"><span data-stu-id="04b52-117">The address and port specified in the first XAddr must be accessible.</span></span> <span data-ttu-id="04b52-118">WSDAPI intenta conectarse a esta dirección al establecer una conexión HTTP.</span><span class="sxs-lookup"><span data-stu-id="04b52-118">WSDAPI attempts to connect to this address when establishing an HTTP connection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04b52-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04b52-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04b52-120">ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="04b52-120">ProbeMatches</span></span>](probematches-message.md)
</dt> <dt>

[<span data-ttu-id="04b52-121">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="04b52-121">ResolveMatches</span></span>](resolvematches-message.md)
</dt> <dt>

[<span data-ttu-id="04b52-122">Patrones de mensajes de intercambio de metadatos y detección</span><span class="sxs-lookup"><span data-stu-id="04b52-122">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



