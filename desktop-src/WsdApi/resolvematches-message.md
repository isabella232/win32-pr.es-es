---
description: Un WS-Discovery mensaje enviado en respuesta a un cliente Resolver mensaje por un servicio correspondiente.
ms.assetid: 0eaa4348-968e-4b45-9509-8b15476edaa1
title: Mensaje ResolveMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140d279a5e66835b7754e3f501732263dff430f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883640"
---
# <a name="resolvematches-message"></a>Mensaje ResolveMatches

Un mensaje ResolveMatches es WS-Discovery mensaje enviado en respuesta al mensaje [Resolver](resolve-message.md) de un cliente por un servicio correspondiente. Para obtener más información sobre los mensajes ResolveMatches, vea la sección 6.2 de la [especificación de WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Unidifusión UDP envía un mensaje ResolveMatches al puerto 3702 (el puerto desde el que se envió el mensaje [Resolver](resolve-message.md) del cliente). ResolveMatches debe enviarse en un plazo de 4 segundos desde el mensaje Resolver; De lo contrario, Windows firewall puede quitar el paquete.

Cualquier aplicación DPWS que envíe [los mensajes resolver](resolve-message.md) recibirá mensajes ResolveMatches.

> [!Note]  
> En este tema se muestra un mensaje DPWS de ejemplo generado por clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes compatibles con DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; use la [herramienta de interoperabilidad básica WSDAPI (WSDBIT) en](https://msdn.microsoft.com/library/cc264250.aspx) su lugar.

 

El siguiente mensaje SOAP muestra un mensaje ResolveMatches de ejemplo.

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
<td>ResolveMatches</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
&lt;/wsa:Action&gt;</code></pre></td>
<td>La acción SOAP ResolveMatches identifica el mensaje como un mensaje ResolveMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:RelatesTo&gt;
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
&lt;/wsa:RelatesTo&gt;</code></pre></td>
<td>Identificador del mensaje al que responde el servicio. Este encabezado coincide con messageId en el <a href="resolve-message.md">mensaje Resolver.</a></td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;6&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Contiene información de secuenciación de aplicaciones, que ayuda a mantener la secuencia de mensajes incluso si se reciben sin orden. AppSequence se valida como se describe en <a href="appsequence-validation-rules.md">Reglas de validación de AppSequence</a>.</td>
</tr>
<tr class="even">
<td>Dirección</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Contiene la dirección del punto de conexión que se va a resolver.</td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:XAddrs&gt;
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsd:XAddrs&gt;</code></pre></td>
<td>XAddrs son direcciones de transporte que se pueden usar para la comunicación entre el cliente y el servicio. Los agregarres se validan como se describe en <a href="xaddr-validation-rules.md">Reglas de validación de XAddr</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de detección y Exchange metadatos](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Resolver mensaje](resolve-message.md)
</dt> </dl>

 

 



