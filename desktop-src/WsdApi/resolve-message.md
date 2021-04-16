---
description: Un mensaje de WS-Discovery utilizado por un cliente para buscar servicios en la red por nombre.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Resolver mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3390d97aad972f001b98587c6b5e7cd7ac708b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706133"
---
# <a name="resolve-message"></a><span data-ttu-id="30e67-103">Resolver mensaje</span><span class="sxs-lookup"><span data-stu-id="30e67-103">Resolve Message</span></span>

<span data-ttu-id="30e67-104">Un mensaje de resolución es un mensaje de WS-Discovery usado por un cliente para buscar servicios en la red por nombre.</span><span class="sxs-lookup"><span data-stu-id="30e67-104">A Resolve message is a WS-Discovery message used by a client to search for services on the network by name.</span></span> <span data-ttu-id="30e67-105">Un cliente solo enviará un mensaje de resolución cuando se envíe un mensaje HTTP (como una [solicitud de intercambio de metadatos o](get--metadata-exchange--http-request-and-message.md) un mensaje de servicio).</span><span class="sxs-lookup"><span data-stu-id="30e67-105">A client will only send a Resolve message when an HTTP message (such as a [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange request or a service message) will be sent.</span></span> <span data-ttu-id="30e67-106">Para obtener más información sobre cómo resolver mensajes, consulte la sección 6,1 de la [especificación WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span><span class="sxs-lookup"><span data-stu-id="30e67-106">For more information about Resolve messages, see section 6.1 of the [WS-Discovery Specification](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span></span>

<span data-ttu-id="30e67-107">Un mensaje de resolución se envía mediante multidifusión de UDP al puerto 3702.</span><span class="sxs-lookup"><span data-stu-id="30e67-107">A Resolve message is sent by UDP multicast to port 3702.</span></span> <span data-ttu-id="30e67-108">No se admite la resolución de mensajes de unidifusión.</span><span class="sxs-lookup"><span data-stu-id="30e67-108">Unicast Resolve messages are not supported.</span></span>

<span data-ttu-id="30e67-109">Los clientes de DPWS envían mensajes de resolución.</span><span class="sxs-lookup"><span data-stu-id="30e67-109">DPWS clients send Resolve messages.</span></span> <span data-ttu-id="30e67-110">En la lista siguiente se muestran los escenarios en los que WSDAPI enviará un mensaje de resolución.</span><span class="sxs-lookup"><span data-stu-id="30e67-110">The following list shows scenarios in which WSDAPI will send a Resolve message.</span></span>

-   <span data-ttu-id="30e67-111">Un cliente de detección de funciones envía un mensaje de resolución si no se incluye ningún XAddrs en un mensaje [ProbeMatches](probematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="30e67-111">A Function Discovery client sends a Resolve message if no XAddrs are included in a [ProbeMatches](probematches-message.md) message.</span></span>
-   <span data-ttu-id="30e67-112">Un cliente que llama a los métodos [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) enviará un mensaje de resolución.</span><span class="sxs-lookup"><span data-stu-id="30e67-112">A client calling the [**IWSDiscoveryProvider::SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) methods will send a Resolve message.</span></span>
-   <span data-ttu-id="30e67-113">Un cliente que llama a [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) puede enviar un mensaje de resolución si se pasa una dirección de dispositivo lógico a *pszDeviceId*.</span><span class="sxs-lookup"><span data-stu-id="30e67-113">A client calling [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) may send a Resolve message if a logical device address is passed to *pszDeviceId*.</span></span>
-   <span data-ttu-id="30e67-114">Un cliente que llama a [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) enviará un mensaje de resolución si se llama a la función con el parámetro pDeviceAddress establecido en **null**.</span><span class="sxs-lookup"><span data-stu-id="30e67-114">A client calling [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) will send a Resolve message if the function is called with the pDeviceAddress parameter set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="30e67-115">En este tema se muestra un mensaje de DPWS de ejemplo generado por los clientes y hosts de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="30e67-115">This topic shows a sample DPWS message generated by WSDAPI clients and hosts.</span></span> <span data-ttu-id="30e67-116">WSDAPI analizará y aceptará otros mensajes conformes a DPWS que no se ajusten a este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="30e67-116">WSDAPI will parse and accept other DPWS-compliant messages that do not conform to this sample.</span></span> <span data-ttu-id="30e67-117">No use este ejemplo para comprobar la interoperabilidad de DPWS; en su lugar, use la [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .</span><span class="sxs-lookup"><span data-stu-id="30e67-117">Do not use this sample to verify DPWS interoperability; use the [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) instead.</span></span>

 

<span data-ttu-id="30e67-118">El siguiente mensaje SOAP muestra un mensaje de resolución de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="30e67-118">The following SOAP message shows a sample Resolve message.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
urn:schemas-xmlsoap-org:ws:2005:04:discovery
</wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Resolve>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Resolve>
</soap:Body>
</soap:Envelope>
```

<span data-ttu-id="30e67-119">Un mensaje de resolución tiene los siguientes puntos de enfoque.</span><span class="sxs-lookup"><span data-stu-id="30e67-119">A Resolve message has the following focus points.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30e67-120">Punto de enfoque</span><span class="sxs-lookup"><span data-stu-id="30e67-120">Focus point</span></span></th>
<th><span data-ttu-id="30e67-121">XML</span><span class="sxs-lookup"><span data-stu-id="30e67-121">XML</span></span></th>
<th><span data-ttu-id="30e67-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="30e67-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30e67-123">Resolver</span><span class="sxs-lookup"><span data-stu-id="30e67-123">Resolve</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td><span data-ttu-id="30e67-124">La acción resolver SOAP identifica el mensaje como un mensaje de resolución.</span><span class="sxs-lookup"><span data-stu-id="30e67-124">The Resolve SOAP action identifies the message as a Resolve message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30e67-125">MessageID</span><span class="sxs-lookup"><span data-stu-id="30e67-125">MessageID</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td><span data-ttu-id="30e67-126">Contiene el identificador de mensaje, al que se hace referencia en un mensaje <a href="resolvematches-message.md">ResolveMatches</a> .</span><span class="sxs-lookup"><span data-stu-id="30e67-126">Contains the message identifier, which is referenced in a <a href="resolvematches-message.md">ResolveMatches</a> message.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30e67-127">Dirección</span><span class="sxs-lookup"><span data-stu-id="30e67-127">Address</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td><span data-ttu-id="30e67-128">Contiene la dirección del extremo que se está resolviendo.</span><span class="sxs-lookup"><span data-stu-id="30e67-128">Contains the address of the endpoint being resolved.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="30e67-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30e67-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e67-130">Mensajes de intercambio de metadatos y detección</span><span class="sxs-lookup"><span data-stu-id="30e67-130">Discovery and Metadata Exchange Messages</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[<span data-ttu-id="30e67-131">Mensaje ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="30e67-131">ResolveMatches Message</span></span>](resolvematches-message.md)
</dt> </dl>

 

 



