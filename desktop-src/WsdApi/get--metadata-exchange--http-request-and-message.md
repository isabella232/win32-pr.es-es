---
description: Mensaje WS-Transfer se usa para solicitar metadatos.
ms.assetid: 18bf27aa-6ae5-4419-ae68-6df9eda10cd4
title: Obtener (metadatos Exchange) solicitud HTTP y mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9cf6241b38f7fa81cc5d9a7c21a0f5e1a406aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567189"
---
# <a name="get-metadata-exchange-http-request-and-message"></a>Obtener (metadatos Exchange) solicitud HTTP y mensaje

Un mensaje Get es un WS-Transfer que se usa para solicitar metadatos. Para obtener más información sobre Obtener mensajes, vea la sección 3.1 de la [especificación de WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf). Dado que el intercambio de metadatos se realiza a través de HTTP, un mensaje Get es la carga de una solicitud HTTP.

Los clientes de DPWS envían mensajes Get. Los clientes de detección de funciones, los clientes WSDAPI que llaman a [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)y los clientes WSDAPI que llaman a [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) envían este mensaje.

> [!Note]  
> En este tema se muestra un mensaje DPWS de ejemplo generado por clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes compatibles con DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; use la [herramienta de interoperabilidad básica WSDAPI (WSDBIT) en](https://msdn.microsoft.com/library/cc264250.aspx) su lugar.

 

En el ejemplo siguiente se muestra una solicitud HTTP Get de ejemplo.

``` syntax
POST /37f86d35-e6ac-4241-964f-1d9ae46fb366
HTTP/1.1
Content-Type: application/soap+xml
User-Agent: WSDAPI
Host: 192.168.0.2:5357
Content-Length: 658
Connection: Keep-Alive
Cache-Control: no-cache
Pragma: no-cache
```

Una solicitud Get HTTP tiene los siguientes puntos de enfoque.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Punto de enfoque</th>
<th>Línea de encabezado</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ruta de acceso URL</td>
<td><pre class="syntax" data-space="preserve"><code>POST /37f86d35-e6ac-4241-964f-1d9ae46fb366</code></pre></td>
<td>Ruta de acceso url donde se publicó la solicitud Get HTTP.</td>
</tr>
<tr class="even">
<td>Host y puerto</td>
<td><pre class="syntax" data-space="preserve"><code>Host: 192.168.0.2:5357</code></pre></td>
<td>El host y el puerto donde se ha dirigido la solicitud GET HTTP.</td>
</tr>
</tbody>
</table>



 

El siguiente mensaje SOAP muestra un mensaje Get de ejemplo.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing">
<soap:Header>
    <wsa:To>
        urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:MessageID>
    <wsa:ReplyTo>
        <wsa:Address>
            https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        </wsa:Address>
    </wsa:ReplyTo>
    <wsa:From>
        <wsa:Address>
            urn:uuid:49e131df-351a-4ece-9a6f-6a862d31cffa
        </wsa:Address>
    </wsa:From>
</soap:Header>
<soap:Body>
</soap:Body>
```

Un mensaje Get tiene los siguientes puntos de enfoque.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>En</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:To&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:To&gt;</code></pre></td>
<td>Identificador del dispositivo al que se solicitan metadatos.</td>
</tr>
<tr class="even">
<td>Obtener</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
</wsa:Action</code></pre></td>
<td>La acción Obtener SOAP identifica el mensaje como un mensaje Get.</td>
</tr>
<tr class="odd">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:MessageID></code></pre></td>
<td>Contiene el identificador del mensaje, al que se hace referencia en un <a href="getresponse--metadata-exchange--message.md">mensaje GetResponse.</a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de detección y Exchange metadatos](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensaje GetResponse](getresponse--metadata-exchange--message.md)
</dt> </dl>

 

 



