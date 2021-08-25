---
description: Mensaje WS-Discovery enviado por un servicio en respuesta a un mensaje de sondeo de clientes.
ms.assetid: 58d3d016-ae29-4090-9b88-e1125db59c95
title: Mensaje ProbeMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa395557aac7c67a82163066cf1bfbb854348e1c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627871"
---
# <a name="probematches-message"></a>Mensaje ProbeMatches

Un mensaje ProbeMatches es WS-Discovery mensaje enviado por un servicio en respuesta al mensaje probe de [un](probe-message.md) cliente. Para obtener más información sobre los mensajes ProbeMatches, vea la sección 5.3 de la [especificación de WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

El unidifusión UDP envía un mensaje ProbeMatches al puerto desde el que se envió el mensaje [probe](probe-message.md) del cliente. ProbeMatches debe enviarse en un plazo de 4 segundos desde el mensaje probe; De lo contrario, Windows Firewall puede quitar el paquete.

Si no se incluye ningún XAddrs en el mensaje ProbeMatches, el cliente puede enviar un mensaje [resolve](resolve-message.md) mediante multidifusión UDP al puerto 3702. El cliente solo enviará un mensaje Resolver cuando [](get--metadata-exchange--http-request-and-message.md) se envíe un mensaje HTTP (como una solicitud de intercambio de metadatos Get o un mensaje de servicio).

Cualquier aplicación DPWS que envíe mensajes [de](probe-message.md) sondeo recibirá mensajes ProbeMatches.

> [!Note]  
> En este tema se muestra un mensaje DPWS de ejemplo generado por clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes compatibles con DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; use la herramienta de interoperabilidad básica de [WSDAPI (WSDBIT) en](https://msdn.microsoft.com/library/cc264250.aspx) su lugar.

 

El siguiente mensaje SOAP muestra un mensaje ProbeMatches de ejemplo.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:967d0036-fe69-40ad-8191-dd1fc8ef64ab
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="9">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ProbeMatches>
        <wsd:ProbeMatch>
            <wsa:EndpointReference>
                <wsa:Address>
                    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                </wsa:Address>
            </wsa:EndpointReference>
            <wsd:Types>wsdp:Device</wsd:Types>
            <wsd:XAddrs>
                https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsd:XAddrs>
            <wsd:MetadataVersion>2</wsd:MetadataVersion>
        </wsd:ProbeMatch>
    </wsd:ProbeMatches>
</soap:Body>
</soap:Envelope>
```

Un mensaje ProbeMatches tiene los siguientes puntos de enfoque.



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
<td>ProbeMatches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
</wsa:Action></code></pre></td>
<td>La acción SOAP ProbeMatches identifica el mensaje como un mensaje ProbeMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:RelatesTo></code></pre></td>
<td>Identificador del mensaje al que responde el servicio. Este encabezado coincide con el MessageId del <a href="probe-message.md">mensaje de</a> sondeo.</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;9&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contiene información de secuenciación de la aplicación, que ayuda a mantener la secuencia de mensajes incluso si se reciben sin orden. AppSequence se valida como se describe en <a href="appsequence-validation-rules.md">Reglas de validación de AppSequence</a>.</td>
</tr>
<tr class="even">
<td>Dirección</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene la dirección del punto de conexión. Se puede hacer referencia a esta solución en un <a href="resolve-message.md">mensaje resolver.</a></td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs></code></pre></td>
<td>XAddrs son direcciones de transporte que se pueden usar para la comunicación entre el cliente y el servicio. Los adidores se validan como se <a href="xaddr-validation-rules.md">describe en Reglas de validación de XAddr</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de detección y Exchange metadatos](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensaje de sondeo](probe-message.md)
</dt> </dl>

 

 



