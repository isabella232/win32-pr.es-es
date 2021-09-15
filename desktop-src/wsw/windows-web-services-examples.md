---
title: Windows Ejemplos de servicios web
description: En los ejemplos siguientes se muestra cómo usar Windows API de servicios web.
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74aec03c4822fb9ba270076b5127dd37d145fb5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574212"
---
# <a name="windows-web-services-examples"></a>Windows Ejemplos de servicios web

En los ejemplos siguientes se muestra cómo usar Windows API de servicios web.

-   [Ejemplos de modelo de servicio](service-model-examples.md)
-   [Ejemplos de capa de canal TCP](tcp-channel-layer-examples.md)
-   [Ejemplos de capas de canal HTTP](http-channel-layer-examples.md)
-   [Ejemplos de capa de canal UDP](udp-channel-layer-examples.md)
-   [Ejemplos de capas de canal de canalización con nombre](named-pipes-channel-layer-examples.md)
-   [Ejemplos de mensajes](message-examples.md)
-   [Ejemplos XML](xml-examples.md)
-   [Ejemplos de modelos asincrónicos](async-model-examples.md)
-   [Ejemplos de capa de canal de seguridad](security-channel-layer-examples.md)
-   [Ejemplos de replicación de archivos](file-replication-examples.md)

## <a name="service-model-examples"></a>Ejemplos de modelo de servicio

Servicio de calculadora: Cliente: [HttpCalculatorClientExample](httpcalculatorclientexample.md), Servidor: [HttpCalculatorServiceExample](httpcalculatorserviceexample.md).

Servicio de calculadora con seguridad de transporte SSL: Cliente: [HttpCalculatorWithSslClientExample](httpcalculatorwithsslclientexample.md), Servidor: [HttpCalculatorWithSslServiceExample](httpcalculatorwithsslserviceexample.md).

Calculator Service with Username over SSL mixed-mode security: Client: [HttpCalculatorWithUsernameOverSslClientExample](httpcalculatorwithusernameoversslclientexample.md), Server: [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).

Calculator Service with Kerberos over SSL mixed-mode security: Client: [HttpCalculatorWithKerberosOverSslClientExample](httpcalculatorwithkerberosoversslclientexample.md), Server: [HttpCalculatorWithKerberosOverSslServiceExample](httpcalculatorwithkerberosoversslserviceexample.md).

Servicio de pedido de compra: [Cliente: HttpPurchaseOrderClientExample](httppurchaseorderclientexample.md), Servidor: [HttpPurchaseOrderServiceExample](httppurchaseorderserviceexample.md).

Servicio de pedido de compra con seguridad de transporte SSL: Cliente: [HttpPurchaseOrderWithSslClientExample](httppurchaseorderwithsslclientexample.md), Servidor: [HttpPurchaseOrderWithSslServiceExample](httppurchaseorderwithsslserviceexample.md).

Servicio de pedido de compra con nombre de usuario sobre seguridad en modo mixto ssl: Cliente: [HttpPurchaseOrderWithUsernameOverSslClientExample](httppurchaseorderwithusernameoversslclientexample.md), Servidor: [HttpPurchaseOrderWithUserNameOverSslServiceExample](httppurchaseorderwithusernameoversslserviceexample.md).

Servicio de pedido de compra con Kerberos sobre la seguridad en modo mixto de SSL: Cliente: [HttpPurchaseOrderWithKerberosOverSslClientExample](httppurchaseorderwithkerberosoversslclientexample.md), Servidor: [HttpPurchaseOrderWithKerberosOverSslServiceExample](httppurchaseorderwithkerberosoversslserviceexample.md).

Servicio de pedido de compra sin tipo: Servidor: [UnTypedServiceExample](untypedserviceexample.md). Cliente: [UnTypedClientExample](untypedclientexample.md)

Calculadora con sesión: Servidor: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Cliente:[SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md).

Calculadora que usa un canal personalizado y una implementación de agente de escucha: Servidor:[HttpCalculatorWithLayeredChannelServiceExample](httpcalculatorwithlayeredchannelserviceexample.md). Cliente:[HttpCalculatorWithLayeredChannelClientExample](httpcalculatorwithlayeredchannelclientexample.md).

Calculadora que usa un canal codificado: Servidor:[HttpCalculatorWithEncodedChannelServiceExample](httpcalculatorwithencodedchannelserviceexample.md). Cliente:[HttpCalculatorWithEncodedChannelClientExample](httpcalculatorwithencodedchannelclientexample.md).

Servicio que controla solicitudes HTTP sin formato (no SOAP): Cliente:[HttpRawClientExample](httprawclientexample.md). Servidor:[HttpRawServiceExample](httprawserviceexample.md).

Service Operation Abort Notification: Server: [BlockingServiceExample](blockingserviceexample.md). Cliente:[ServiceCancellationExample](servicecancellationexample.md).

Cancelación de llamadas: Servidor: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Cliente:[Llame aAbandoneExample.](callabandonexample.md)

Cree manualmente una descripción de directiva y úsela para crear un proxy de servicio: [PolicyTemplateExample](policytemplateexample.md).

## <a name="tcp-channel-layer-examples"></a>Ejemplos de capa de canal TCP

Un ejemplo de TCP que envía mensajes mediante un patrón unía: Cliente: [OneWayTcpClientExample](onewaytcpclientexample.md), Servidor: [OneWayTcpServerExample](onewaytcpserverexample.md)

Un ejemplo de TCP que envía mensajes mediante un patrón de solicitud-respuesta: Client: [RequestReplyTcpClientExample](requestreplytcpclientexample.md), Server: [RequestReplyTcpServerExample](requestreplytcpserverexample.md)

Un ejemplo tcp de streaming: Cliente: [StreamingTcpClientExample](streamingtcpclientexample.md), Servidor: [StreamingTcpServerExample](streamingtcpserverexample.md)

Un ejemplo de TCP de streaming asincrónico: Cliente: [AsyncStreamingTcpClientExample](asyncstreamingtcpclientexample.md), Servidor: [AsyncStreamingTcpServerExample](asyncstreamingtcpserverexample.md)

## <a name="http-channel-layer-examples"></a>Ejemplos de capas de canal HTTP

Un ejemplo HTTP: Cliente: [HttpClientExample](httpclientexample.md), Servidor: [HttpServerExample](httpserverexample.md)

Un ejemplo HTTP que usa las API de streaming: Cliente: [StreamingHttpClientExample](streaminghttpclientexample.md), Servidor: [StreamingHttpServerExample](streaminghttpserverexample.md)

## <a name="udp-channel-layer-examples"></a>Ejemplos de capa de canal UDP

Un ejemplo de UDP que envía mensajes mediante un patrón unív: [Client: OneWayUdpClientExample](onewayudpclientexample.md), Server: [OneWayUdpServerExample](onewayudpserverexample.md)

Un ejemplo de UDP que envía mensajes mediante un patrón de respuesta de solicitud de multidifusión: Cliente: [MulticastUdpClientExample](multicastudpclientexample.md), Servidor: [MulticastUdpServerExample](multicastudpserverexample.md) El siguiente es el mismo ejemplo, pero con direccionamiento IPv6: Cliente: [MulticastUdpClientExample6](multicastudpclientexample6.md), Servidor: [MulticastUdpServerExample6](multicastudpserverexample6.md)

## <a name="named-pipes-channel-layer-examples"></a>Ejemplos de capas de canal de canal de canal con nombre

Ejemplo de canalizaciones con nombre que envía mensajes mediante un patrón de solicitud-respuesta: Client: [RequestReplyNamedPipesClientExample](requestreplynamedpipesclientexample.md), Server: [RequestReplyNamedPipesServerExample](requestreplynamedpipesserverexample.md)

Ejemplo de canalizaciones con nombre de streaming: Cliente: [StreamingNamedPipesClientExample](streamingnamedpipesclientexample.md), Servidor: [StreamingNamedPipesServerExample](streamingnamedpipesserverexample.md)

## <a name="message-examples"></a>Ejemplos de mensajes

Un ejemplo que usa encabezados de mensaje personalizados: [CustomHeaderExample](customheaderexample.md)

Un ejemplo que codifica y descodifica un mensaje: [MessageEncodingExample](messageencodingexample.md)

Un ejemplo que reenvía un mensaje: [ForwardMessageExample](forwardmessageexample.md)

## <a name="xml-examples"></a>Ejemplos XML

Ejemplo que escribe y lee xml mediante un búfer XML [ReadWriteXmlExample](readwritexmlexample.md)

Ejemplo que escribe y lee datos binarios mediante MTOM, WsWriteBytes, WsPushBytes y WsPullBytes [ReadWriteBytesXmlExample](readwritebytesxmlexample.md)

Ejemplo que navega por un búfer XML [NavigateXmlExample](navigatexmlexample.md)

Ejemplo que lee un nodo de documento XML por nodo [ReadXmlExample](readxmlexample.md)

Un ejemplo que busca y muestra un atributo XML [ReadAttributeExample](readattributeexample.md)

Ejemplo que escribe y lee una matriz de elementos [ReadWriteArrayExample](readwritearrayexample.md)

Ejemplo que inserta un elemento en un búfer XML [InsertElementExample](insertelementexample.md)

Ejemplo que muestra el uso de algunas funciones auxiliares de búfer XML [XmlBufferExample](xmlbufferexample.md)

Ejemplo que escribe y lee el tipo derivado mediante las funciones auxiliares generadas por wsutil [DerivedTypeExample](derivedtypeexample.md)

## <a name="async-model-examples"></a>Ejemplos de modelos asincrónicos

Ejemplo que muestra el modelo para las funciones asincrónicas. [AsyncModelExample](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a>Ejemplos de capa de canal de seguridad

Windows seguridad de transporte a través de TCP: Cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Windows seguridad de transporte en canalizaciones con nombre: Cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Seguridad de transporte SSL: Cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), Servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).

Username over SSL mixed-mode security:Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Username over SSL mixed-mode security: Client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

## <a name="metadata-example"></a>Ejemplo de metadatos

En los ejemplos siguientes se muestra cómo procesar documentos WSDL y de directiva con el objetivo de extraer información sobre qué protocolo admite un punto de conexión.

Nombre de usuario sobre seguridad en modo mixto ssl: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emitido a través de la seguridad en modo mixto de SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificado X509 sobre seguridad en modo mixto SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="ws-metadata-exchange-example"></a>WS-Metadata Exchange ejemplo

En los ejemplos siguientes se muestra cómo habilitar WS-MetadataExchange host [de WS \_ SERVICE \_ ](ws-service-host.md).

Servicio TCP con WS-MetadataExchange habilitado: [MetadataExchangeSample](metadataexchangesample.md). Cliente de moniker de servicio WCF que llama al servicio TCP con WS-MetadataExchange habilitado: [ServiceMonikerSample](servicemonikersample.md).

## <a name="custom-headers-and-service-model"></a>Encabezados personalizados y modelo de servicio

En los ejemplos siguientes se muestra cómo usar encabezados personalizados con [WS \_ SERVICE \_ PROXY](ws-service-proxy.md) y [WS \_ SERVICE \_ HOST,](ws-service-host.md) respectivamente.

Cliente: [HttpCustomHeaderPurchaseOrderClientExample](httpcustomheaderpurchaseorderclientexample.md), Servidor: [HttpCustomHeaderPurchaseOrderServiceExample](httpcustomheaderpurchaseorderserviceexample.md).

## <a name="file-replication-sample"></a>Ejemplo de replicación de archivos

Un ejemplo completo que muestra cómo implementar un servicio de replicación de archivos: [Herramienta: FileRepToolExample](filereptoolexample.md), Servicio: [FileRepServiceExample](filerepserviceexample.md).

## <a name="wcf-public-service-interoperation"></a>Interoperación de servicios públicos wcf

Un Windows web Services se comunica con un cliente de servicio WCF: [WcfPublicServiceSample](wcfpublicservicesample.md).

## <a name="custom-http-proxy"></a>Proxy HTTP personalizado

Un Windows web Services se comunica con un servicio ASMX TerraService mediante el cliente proxy personalizado: [AsmxServiceSampleWithCustomProxy](asmxterraservicesamplewithcustomproxy.md)

 

 




