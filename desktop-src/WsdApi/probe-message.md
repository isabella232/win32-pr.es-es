---
description: Un mensaje de WS-Discovery utilizado por un cliente para buscar servicios en la red por tipo de servicio.
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: Mensaje de sondeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913c163be8d82297a642b1a97a7d28e0c403ca08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155981"
---
# <a name="probe-message"></a>Mensaje de sondeo

Un mensaje de sondeo es un mensaje WS-Discovery utilizado por un cliente para buscar servicios en la red por tipo de servicio. Para obtener más información sobre los mensajes de sondeo, consulte la sección 5,2 de la [especificación WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un mensaje de sondeo se envía mediante multidifusión de UDP al puerto 3702. No se admiten mensajes de sondeo de unidifusión.

Los clientes de DPWS envían mensajes de sondeo. La lista siguiente muestra los escenarios en los que WSDAPI enviará un mensaje de sondeo.

-   Los clientes de detección de funciones envían mensajes de sondeo.
-   Los clientes WSDAPI que llaman a [**IWSDiscoveryProvider:: SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) envían mensajes de sondeo.
-   Los clientes WSDAPI que llaman a [**IWSDiscoveryProvider:: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) envían mensajes de sondeo.
-   Las aplicaciones que usan la detección dirigida envían mensajes de sondeo a través de HTTP o HTTPS.

> [!Note]  
> En este tema se muestra un mensaje de DPWS de ejemplo generado por los clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes conformes a DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; en su lugar, use la [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

El siguiente mensaje SOAP muestra un mensaje de sondeo de ejemplo.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Probe>
        <wsd:Types>wsdp:Device</wsd:Types>
    </wsd:Probe>
</soap:Body>
```

Un mensaje de sondeo tiene los siguientes puntos de enfoque.



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
<td>Sondeo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
</wsa:Action></code></pre></td>
<td>La acción SOAP de sondeo identifica el mensaje como un mensaje de sondeo.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:MessageID></code></pre></td>
<td>Contiene el identificador de mensaje al que hace referencia el elemento latesto en un mensaje <a href="probematches-message.md">ProbeMatches</a> .</td>
</tr>
<tr class="odd">
<td>Tipos</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Contiene los tipos de WS-Discovery para los que el cliente está buscando. Este elemento no debe estar vacío.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Mensaje ProbeMatches](probematches-message.md)
</dt> </dl>

 

 



