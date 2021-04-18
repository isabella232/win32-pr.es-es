---
description: Un mensaje de WS-Discovery enviado en respuesta a un mensaje de resolución de los clientes por un servicio coincidente.
ms.assetid: 0eaa4348-968e-4b45-9509-8b15476edaa1
title: Mensaje ResolveMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ab5c0d66541b93eeee13966d686c94eef9364d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707257"
---
# <a name="resolvematches-message"></a>Mensaje ResolveMatches

Un mensaje de ResolveMatches es un mensaje WS-Discovery enviado en respuesta al mensaje de [resolución](resolve-message.md) de un cliente mediante un servicio coincidente. Para obtener más información acerca de los mensajes de ResolveMatches, consulte la sección 6,2 de la [especificación WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Una unidifusión UDP envía un mensaje ResolveMatches al puerto 3702 (el puerto desde el que se envió el mensaje de [resolución](resolve-message.md) del cliente). ResolveMatches se debe enviar en los 4 segundos del mensaje de resolución; de lo contrario, el Firewall de Windows puede quitar el paquete.

Cualquier aplicación DPWS que envíe mensajes de [resolución](resolve-message.md) recibirá mensajes ResolveMatches.

> [!Note]  
> En este tema se muestra un mensaje de DPWS de ejemplo generado por los clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes conformes a DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; en su lugar, use la [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

El siguiente mensaje SOAP muestra un mensaje de ResolveMatches de ejemplo.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:64ddd01c-b0d6-4afd-aba6-6f1f161ce9d4
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="6">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ResolveMatches>
        <wsd:ResolveMatch>
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
        </wsd:ResolveMatch>
    </wsd:ResolveMatches>
</soap:Body>
</soap:Envelope>
```

Un mensaje ResolveMatches tiene los siguientes puntos de enfoque.



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
<td>ResolveMatches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
</wsa:Action></code></pre></td>
<td>La acción SOAP ResolveMatches identifica el mensaje como un mensaje ResolveMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:RelatesTo></code></pre></td>
<td>Identificador del mensaje al que responde el servicio. Este encabezado coincide con el MessageId del mensaje de <a href="resolve-message.md">resolución</a> .</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;6&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contiene información de secuenciación de aplicaciones, que ayuda a mantener la secuencia de mensajes incluso si se reciben desordenados. El AppSequence se valida como se describe en <a href="appsequence-validation-rules.md">reglas de validación de AppSequence</a>.</td>
</tr>
<tr class="even">
<td>Dirección</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene la dirección del extremo que se está resolviendo.</td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs></code></pre></td>
<td>XAddrs son direcciones de transporte que se pueden usar para la comunicación entre el cliente y el servicio. Las direcciones se validan como se describe en <a href="xaddr-validation-rules.md">reglas de validación de XAddr</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Resolver mensaje](resolve-message.md)
</dt> </dl>

 

 



