---
description: WS-Transfer mensaje que se usa para responder a una solicitud de metadatos.
ms.assetid: aff05317-35db-4ea6-9692-1e09e4682fe7
title: GetResponse (intercambio de metadatos), mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b91546076698f17a25b8a87444ae3eca71d65a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276973"
---
# <a name="getresponse-metadata-exchange-message"></a>GetResponse (intercambio de metadatos), mensaje

Un mensaje GetResponse es un mensaje WS-Transfer que se usa para responder a una solicitud de metadatos. Para obtener más información acerca de los mensajes GetResponse, consulte la sección 3,1 de la [especificación WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf).

Cualquier aplicación DPWS que envíe mensajes [Get](get--metadata-exchange--http-request-and-message.md) recibirá mensajes GetResponse.

> [!Note]  
> En este tema se muestra un mensaje de DPWS de ejemplo generado por los clientes y hosts de WSDAPI. WSDAPI analizará y aceptará otros mensajes conformes a DPWS que no se ajusten a este ejemplo. No use este ejemplo para comprobar la interoperabilidad de DPWS; en su lugar, use la [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

El siguiente mensaje SOAP muestra un mensaje de ejemplo GetResponse.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof"
    xmlns:sim="https://schemas.example.org/SimpleService"
    xmlns:att="https://schemas.example.org/AttachmentService"
    xmlns:eve="https://schemas.example.org/EventingService">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:119dcdf5-fc0d-4d40-bf1f-de52dc292744
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:RelatesTo>
</soap:Header>
<soap:Body>
    <wsx:Metadata>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice">
            <wsdp:ThisDevice>
                <wsdp:FriendlyName>
                    WSDAPI Basic Interop Server
                </wsdp:FriendlyName>
                <wsdp:FirmwareVersion>alpha</wsdp:FirmwareVersion>
                <wsdp:SerialNumber>1</wsdp:SerialNumber>
            </wsdp:ThisDevice>
        </wsx:MetadataSection>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel">
            <wsdp:ThisModel>
                <wsdp:Manufacturer>
                    Microsoft
                </wsdp:Manufacturer>
                <wsdp:ManufacturerUrl>
                    https://www.microsoft.com/
                </wsdp:ManufacturerUrl>
                <wsdp:ModelName>
                    WSDAPI Interop device
                </wsdp:ModelName>
                <wsdp:ModelNumber>0.1</wsdp:ModelNumber>
                <wsdp:ModelUrl>
                    https://www.microsoft.com/
                </wsdp:ModelUrl>
                <wsdp:PresentationUrl>
                    https://www.microsoft.com/
                </wsdp:PresentationUrl>
            </wsdp:ThisModel>
        </wsx:MetadataSection>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship">
            <wsdp:Relationship Type="https://schemas.xmlsoap.org/ws/2006/02/devprof/host">
                <wsdp:Host>
                    <wsa:EndpointReference>
                        <wsa:Address>
                            urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                        </wsa:Address>
                    </wsa:EndpointReference>
                    <wsdp:Types>sim:SimpleDeviceType</wsdp:Types>
                    <wsdp:ServiceId>
                        https://testdevice.interop/SimpleDevice
                    </wsdp:ServiceId>
                </wsdp:Host>
                <wsdp:Hosted>
                    <wsa:EndpointReference>
                        <wsa:Address>
                            https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
                        </wsa:Address>
                    </wsa:EndpointReference>
                    <wsdp:Types>sim:SimpleService</wsdp:Types>
                    <wsdp:ServiceId>
                        https://testdevice.interop/SimpleService1
                    </wsdp:ServiceId>
                </wsdp:Hosted>
            </wsdp:Relationship>
        </wsx:MetadataSection>
    </wsx:Metadata>
</soap:Body>
</soap:Envelope>
```

Un mensaje GetResponse tiene los siguientes puntos de enfoque.



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
<td>GetResponse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse
</wsa:Action></code></pre></td>
<td>La acción de SOAP GetResponse identifica el mensaje como un mensaje GetResponse.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:RelatesTo></code></pre></td>
<td>Identificador del mensaje al que responde el dispositivo. Este encabezado coincide con el MessageID del mensaje <a href="get--metadata-exchange--http-request-and-message.md">Get</a> .</td>
</tr>
<tr class="odd">
<td>Dirección</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene la dirección del punto de conexión de los servicios hospedados en este dispositivo.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Obtener mensaje](get--metadata-exchange--http-request-and-message.md)
</dt> </dl>

 

 



