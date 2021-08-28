---
description: Mensaje WS-Discovery que se usa para anunciar la salida de un dispositivo o servicio de la red.
ms.assetid: 7b9abfcc-28ab-4f29-af69-6dc68e3f51b6
title: Mensaje de adiós
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb512694833de013ab116561a2e01d0f7b0f9463
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887191"
---
# <a name="bye-message"></a>Mensaje de adiós

Un mensaje de adiós es un WS-Discovery que se usa para anunciar la salida de un dispositivo o servicio de la red. Para obtener más información sobre los mensajes de adiós, vea la sección 4.2 de [la especificación WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Los mensajes de adiós no se han solicitado. Los mensajes son opcionales.

> [!Note]  
> En este tema se muestra un mensaje DPWS de ejemplo generado por clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes compatibles con DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; use la [herramienta de interoperabilidad básica WSDAPI (WSDBIT) en](https://msdn.microsoft.com/library/cc264250.aspx) su lugar.

 

El siguiente mensaje SOAP muestra un mensaje de adiós de ejemplo.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:193ccfa0-347d-41a1-9285-f500b6b96a15
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="21">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Bye>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Bye>
</soap:Body>
```

Un mensaje de adiós tiene los siguientes puntos de enfoque.



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
<td>Adiós</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
&lt;/wsa:Action&gt;</code></pre></td>
<td>La acción Bye SOAP identifica el mensaje como un mensaje de adiós.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;21&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Contiene información de secuenciación de aplicaciones, que ayuda a mantener la secuencia de mensajes incluso si se reciben sin orden. AppSequence se valida como se describe en <a href="appsequence-validation-rules.md">Reglas de validación de AppSequence</a>.</td>
</tr>
<tr class="odd">
<td>Dirección</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Contiene la dirección del punto de conexión sin conexión.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de detección y Exchange metadatos](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensaje hello](hello-message.md)
</dt> </dl>

 

 



