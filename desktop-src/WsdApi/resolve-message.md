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
# <a name="resolve-message"></a>Resolver mensaje

Un mensaje de resolución es un mensaje de WS-Discovery usado por un cliente para buscar servicios en la red por nombre. Un cliente solo enviará un mensaje de resolución cuando se envíe un mensaje HTTP (como una [solicitud de intercambio de metadatos o](get--metadata-exchange--http-request-and-message.md) un mensaje de servicio). Para obtener más información sobre cómo resolver mensajes, consulte la sección 6,1 de la [especificación WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un mensaje de resolución se envía mediante multidifusión de UDP al puerto 3702. No se admite la resolución de mensajes de unidifusión.

Los clientes de DPWS envían mensajes de resolución. En la lista siguiente se muestran los escenarios en los que WSDAPI enviará un mensaje de resolución.

-   Un cliente de detección de funciones envía un mensaje de resolución si no se incluye ningún XAddrs en un mensaje [ProbeMatches](probematches-message.md) .
-   Un cliente que llama a los métodos [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) enviará un mensaje de resolución.
-   Un cliente que llama a [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) puede enviar un mensaje de resolución si se pasa una dirección de dispositivo lógico a *pszDeviceId*.
-   Un cliente que llama a [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) enviará un mensaje de resolución si se llama a la función con el parámetro pDeviceAddress establecido en **null**.

> [!Note]  
> En este tema se muestra un mensaje de DPWS de ejemplo generado por los clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes conformes a DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; en su lugar, use la [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

El siguiente mensaje SOAP muestra un mensaje de resolución de ejemplo.

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

Un mensaje de resolución tiene los siguientes puntos de enfoque.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Punto de enfoque</th>
<th>XML</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resolver</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td>La acción resolver SOAP identifica el mensaje como un mensaje de resolución.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Contiene el identificador de mensaje, al que se hace referencia en un mensaje <a href="resolvematches-message.md">ResolveMatches</a> .</td>
</tr>
<tr class="odd">
<td>Dirección</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene la dirección del extremo que se está resolviendo.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensaje ResolveMatches](resolvematches-message.md)
</dt> </dl>

 

 



