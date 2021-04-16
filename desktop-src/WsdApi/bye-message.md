---
description: Un mensaje de WS-Discovery que se usa para anunciar la salida de un dispositivo o servicio de la red.
ms.assetid: 7b9abfcc-28ab-4f29-af69-6dc68e3f51b6
title: Mensaje bye
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26880e8b1d4eae7f366f797017b033f9f444fe1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546507"
---
# <a name="bye-message"></a>Mensaje bye

Un mensaje bye es un mensaje WS-Discovery que se usa para anunciar la salida de un dispositivo o servicio de la red. Para obtener más información acerca de los mensajes bye, consulte la sección 4,2 de la [especificación WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Los mensajes adiós no se solicitan. Los mensajes son opcionales.

> [!Note]  
> En este tema se muestra un mensaje de DPWS de ejemplo generado por los clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes conformes a DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; en su lugar, use la [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

El siguiente mensaje SOAP muestra un mensaje bye de ejemplo.

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

Un mensaje bye tiene los siguientes puntos de enfoque.



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
<td>Adiós</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
</wsa:Action></code></pre></td>
<td>La acción bye SOAP identifica el mensaje como un mensaje bye.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;21&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contiene información de secuenciación de aplicaciones, que ayuda a mantener la secuencia de mensajes incluso si se reciben desordenados. El AppSequence se valida como se describe en <a href="appsequence-validation-rules.md">reglas de validación de AppSequence</a>.</td>
</tr>
<tr class="odd">
<td>Dirección</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene la dirección del extremo que se va a desconectar.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensaje de Hola](hello-message.md)
</dt> </dl>

 

 



