---
description: Mensaje WS-Discovery que usa un cliente para buscar servicios en la red por nombre.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Resolver mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54887db566ee428e6bfe9ec2de9016a637884b092611a85e607c55aaa4176abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991615"
---
# <a name="resolve-message"></a>Resolver mensaje

Un mensaje resolver es un WS-Discovery utilizado por un cliente para buscar servicios en la red por nombre. Un cliente solo enviará un mensaje Resolver cuando se envíe un mensaje HTTP (como una solicitud [de](get--metadata-exchange--http-request-and-message.md) intercambio de metadatos Get o un mensaje de servicio). Para obtener más información sobre la resolución de mensajes, vea la sección 6.1 de [la especificación de WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

La multidifusión UDP envía un mensaje resolver al puerto 3702. No se admiten mensajes de resolución de unidifusión.

Los clientes DPWS envían mensajes resolver. En la lista siguiente se muestran escenarios en los que WSDAPI enviará un mensaje Resolver.

-   Un cliente de detección de funciones envía un mensaje Resolver si no se incluye ningún XAddrs en un [mensaje ProbeMatches.](probematches-message.md)
-   Un cliente que llama [**a los métodos IWSDiscoveryProvider::SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) enviará un mensaje Resolve.
-   Un cliente que llama a [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) puede enviar un mensaje Resolver si se pasa una dirección de dispositivo lógico a *pszDeviceId*.
-   Un cliente que llama a [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) enviará un mensaje Resolver si se llama a la función con el parámetro pDeviceAddress establecido en **NULL.**

> [!Note]  
> En este tema se muestra un mensaje DPWS de ejemplo generado por clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes compatibles con DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; use la [herramienta de interoperabilidad básica WSDAPI (WSDBIT) en](https://msdn.microsoft.com/library/cc264250.aspx) su lugar.

 

El siguiente mensaje SOAP muestra un ejemplo de resolución de mensaje.

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

Un mensaje Resolver tiene los siguientes puntos de enfoque.



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
<td>La acción Resolver SOAP identifica el mensaje como un mensaje resolver.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Contiene el identificador del mensaje, al que se hace referencia en un <a href="resolvematches-message.md">mensaje ResolveMatches.</a></td>
</tr>
<tr class="odd">
<td>Dirección</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene la dirección del punto de conexión que se va a resolver.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de detección y Exchange metadatos](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensaje ResolveMatches](resolvematches-message.md)
</dt> </dl>

 

 



