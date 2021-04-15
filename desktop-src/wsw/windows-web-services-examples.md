---
title: Ejemplos de servicios Web de Windows
description: En los siguientes ejemplos se muestra cómo usar la API de servicios Web de Windows.
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74aec03c4822fb9ba270076b5127dd37d145fb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714137"
---
# <a name="windows-web-services-examples"></a>Ejemplos de servicios Web de Windows

En los siguientes ejemplos se muestra cómo usar la API de servicios Web de Windows.

-   [Ejemplos de modelos de servicio](service-model-examples.md)
-   [Ejemplos de capas de canales TCP](tcp-channel-layer-examples.md)
-   [Ejemplos de capas de canales HTTP](http-channel-layer-examples.md)
-   [Ejemplos de capas de canales UDP](udp-channel-layer-examples.md)
-   [Ejemplos de capas de canal de canalización con nombre](named-pipes-channel-layer-examples.md)
-   [Ejemplos de mensajes](message-examples.md)
-   [Ejemplos de XML](xml-examples.md)
-   [Ejemplos de modelos asincrónicos](async-model-examples.md)
-   [Ejemplos de capas de canales de seguridad](security-channel-layer-examples.md)
-   [Ejemplos de replicación de archivos](file-replication-examples.md)

## <a name="service-model-examples"></a>Ejemplos de modelos de servicio

Servicio de calculadora: cliente: [HttpCalculatorClientExample](httpcalculatorclientexample.md), servidor: [HttpCalculatorServiceExample](httpcalculatorserviceexample.md).

Servicio de calculadora con seguridad de transporte SSL: cliente: [HttpCalculatorWithSslClientExample](httpcalculatorwithsslclientexample.md), servidor: [HttpCalculatorWithSslServiceExample](httpcalculatorwithsslserviceexample.md).

Servicio de calculadora con el nombre de usuario sobre la seguridad de modo mixto de SSL: cliente: [HttpCalculatorWithUsernameOverSslClientExample](httpcalculatorwithusernameoversslclientexample.md), servidor: [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).

Servicio de calculadora con Kerberos sobre la seguridad de modo mixto de SSL: cliente: [HttpCalculatorWithKerberosOverSslClientExample](httpcalculatorwithkerberosoversslclientexample.md), servidor: [HttpCalculatorWithKerberosOverSslServiceExample](httpcalculatorwithkerberosoversslserviceexample.md).

Servicio de pedido de compra: cliente: [HttpPurchaseOrderClientExample](httppurchaseorderclientexample.md), servidor: [HttpPurchaseOrderServiceExample](httppurchaseorderserviceexample.md).

Servicio de pedido de compra con seguridad de transporte SSL: cliente: [HttpPurchaseOrderWithSslClientExample](httppurchaseorderwithsslclientexample.md), servidor: [HttpPurchaseOrderWithSslServiceExample](httppurchaseorderwithsslserviceexample.md).

Servicio de pedido de compra con el nombre de usuario sobre la seguridad de modo mixto de SSL: cliente: [HttpPurchaseOrderWithUsernameOverSslClientExample](httppurchaseorderwithusernameoversslclientexample.md), servidor: [HttpPurchaseOrderWithUserNameOverSslServiceExample](httppurchaseorderwithusernameoversslserviceexample.md).

Servicio de pedido de compra con Kerberos a través de SSL en modo mixto: cliente: [HttpPurchaseOrderWithKerberosOverSslClientExample](httppurchaseorderwithkerberosoversslclientexample.md), servidor: [HttpPurchaseOrderWithKerberosOverSslServiceExample](httppurchaseorderwithkerberosoversslserviceexample.md).

Servicio de pedido de compra sin tipo: servidor: [UnTypedServiceExample](untypedserviceexample.md). Cliente: [UnTypedClientExample](untypedclientexample.md)

Calculadora con sesión: servidor: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Cliente:[SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md).

Calculadora mediante un canal personalizado y una implementación de agente de escucha: servidor:[HttpCalculatorWithLayeredChannelServiceExample](httpcalculatorwithlayeredchannelserviceexample.md). Cliente:[HttpCalculatorWithLayeredChannelClientExample](httpcalculatorwithlayeredchannelclientexample.md).

Calculadora mediante un canal codificado: servidor:[HttpCalculatorWithEncodedChannelServiceExample](httpcalculatorwithencodedchannelserviceexample.md). Cliente:[HttpCalculatorWithEncodedChannelClientExample](httpcalculatorwithencodedchannelclientexample.md).

Servicio que administra las solicitudes HTTP sin procesar (no SOAP): Client:[HttpRawClientExample](httprawclientexample.md). Servidor:[HttpRawServiceExample](httprawserviceexample.md).

Notificación de anulación de operación de servicio: servidor: [BlockingServiceExample](blockingserviceexample.md). Cliente:[ServiceCancellationExample](servicecancellationexample.md).

Cancelación de llamada: servidor: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Cliente:[CallAbandonExample](callabandonexample.md).

Cree manualmente una descripción de directiva y Úsela para crear un proxy de servicio: [PolicyTemplateExample](policytemplateexample.md).

## <a name="tcp-channel-layer-examples"></a>Ejemplos de capas de canales TCP

Ejemplo de TCP que envía mensajes mediante un patrón unidireccional: cliente: [OneWayTcpClientExample](onewaytcpclientexample.md), servidor: [OneWayTcpServerExample](onewaytcpserverexample.md)

Un ejemplo de TCP que envía mensajes mediante un patrón de solicitud-respuesta: cliente: [RequestReplyTcpClientExample](requestreplytcpclientexample.md), servidor: [RequestReplyTcpServerExample](requestreplytcpserverexample.md)

Un ejemplo de TCP de streaming: cliente: [StreamingTcpClientExample](streamingtcpclientexample.md), servidor: [StreamingTcpServerExample](streamingtcpserverexample.md)

Un ejemplo de TCP de streaming asincrónico: cliente: [AsyncStreamingTcpClientExample](asyncstreamingtcpclientexample.md), servidor: [AsyncStreamingTcpServerExample](asyncstreamingtcpserverexample.md)

## <a name="http-channel-layer-examples"></a>Ejemplos de capas de canales HTTP

Un ejemplo de HTTP: Client: [HttpClientExample](httpclientexample.md), Server: [HttpServerExample](httpserverexample.md)

Un ejemplo de HTTP que usa las API de streaming: Client: [StreamingHttpClientExample](streaminghttpclientexample.md), Server: [StreamingHttpServerExample](streaminghttpserverexample.md)

## <a name="udp-channel-layer-examples"></a>Ejemplos de capas de canales UDP

Un ejemplo de UDP que envía mensajes con un patrón unidireccional: cliente: [OneWayUdpClientExample](onewayudpclientexample.md), servidor: [OneWayUdpServerExample](onewayudpserverexample.md)

Un ejemplo de UDP que envía mensajes mediante un patrón de respuesta de solicitud de multidifusión: Client: [MulticastUdpClientExample](multicastudpclientexample.md), Server: [MulticastUdpServerExample](multicastudpserverexample.md) el siguiente ejemplo es el mismo, pero el uso de direcciones IPv6: Client: [MulticastUdpClientExample6](multicastudpclientexample6.md), Server: [MulticastUdpServerExample6](multicastudpserverexample6.md)

## <a name="named-pipes-channel-layer-examples"></a>Ejemplos de capas de canal de canalizaciones con nombre

Un ejemplo de canalizaciones con nombre que envía mensajes mediante un patrón de solicitud-respuesta: cliente: [RequestReplyNamedPipesClientExample](requestreplynamedpipesclientexample.md), servidor: [RequestReplyNamedPipesServerExample](requestreplynamedpipesserverexample.md)

Un streaming denominado Pipes ejemplo: Client: [StreamingNamedPipesClientExample](streamingnamedpipesclientexample.md), Server: [StreamingNamedPipesServerExample](streamingnamedpipesserverexample.md)

## <a name="message-examples"></a>Ejemplos de mensajes

Un ejemplo que usa encabezados de mensaje personalizados: [CustomHeaderExample](customheaderexample.md)

Un ejemplo que codifica y descodifica un mensaje: [MessageEncodingExample](messageencodingexample.md)

Un ejemplo que reenvía un mensaje: [ForwardMessageExample](forwardmessageexample.md)

## <a name="xml-examples"></a>Ejemplos de XML

Ejemplo que escribe y lee XML mediante un búfer XML [ReadWriteXmlExample](readwritexmlexample.md)

Un ejemplo que escribe y lee datos binarios mediante MTOM, WsWriteBytes, WsPushBytes y WsPullBytes [ReadWriteBytesXmlExample](readwritebytesxmlexample.md)

Ejemplo que navega por un búfer XML [NavigateXmlExample](navigatexmlexample.md)

Ejemplo que lee un nodo de documento XML por nodo [ReadXmlExample](readxmlexample.md)

Un ejemplo en el que se encuentra y muestra un atributo XML [ReadAttributeExample](readattributeexample.md)

Un ejemplo que escribe y Lee una matriz de elementos [ReadWriteArrayExample](readwritearrayexample.md)

Un ejemplo que inserta un elemento en un búfer XML [InsertElementExample](insertelementexample.md)

Un ejemplo que muestra el uso de algunas funciones auxiliares de búfer de XML [XmlBufferExample](xmlbufferexample.md)

Un ejemplo que escribe y lee el tipo derivado mediante las funciones auxiliares generadas por wsutil [DerivedTypeExample](derivedtypeexample.md)

## <a name="async-model-examples"></a>Ejemplos de modelos asincrónicos

Un ejemplo que ilustra el modelo para las funciones asincrónicas. [AsyncModelExample](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a>Ejemplos de capas de canales de seguridad

Seguridad de transporte de Windows a través de TCP: cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Seguridad de transporte de Windows a través de canalizaciones con nombre: cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Seguridad de transporte SSL: cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nombre de usuario sobre SSL en modo mixto: cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nombre de usuario sobre SSL en modo mixto: cliente: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), servidor: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

## <a name="metadata-example"></a>Ejemplo de metadatos

En los siguientes ejemplos se muestra cómo procesar documentos WSDL y de directiva con el objetivo de extraer información sobre el protocolo que admite un extremo.

Nombre de usuario sobre la seguridad de modo mixto de SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emitido sobre seguridad de modo mixto de SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificado X509 sobre seguridad de modo mixto de SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="ws-metadata-exchange-example"></a>Ejemplo de WS-Metadata Exchange

En los siguientes ejemplos se muestra cómo habilitar WS-MetadataExchange en el [ \_ \_ host del servicio WS](ws-service-host.md).

Servicio TCP con WS-MetadataExchange habilitada: [MetadataExchangeSample](metadataexchangesample.md). Cliente de moniker del servicio WCF que llama al servicio TCP con WS-MetadataExchange habilitada: [ServiceMonikerSample](servicemonikersample.md).

## <a name="custom-headers-and-service-model"></a>Encabezados personalizados y modelo de servicio

En los siguientes ejemplos se muestra cómo usar encabezados personalizados con [el \_ \_ proxy de servicio WS](ws-service-proxy.md) y el [ \_ \_ host de servicio WS](ws-service-host.md) , respectivamente.

Cliente: [HttpCustomHeaderPurchaseOrderClientExample](httpcustomheaderpurchaseorderclientexample.md), servidor: [HttpCustomHeaderPurchaseOrderServiceExample](httpcustomheaderpurchaseorderserviceexample.md).

## <a name="file-replication-sample"></a>Ejemplo de replicación de archivos

Un ejemplo completo que muestra cómo implementar un servicio de replicación de archivos: Tool: [FileRepToolExample](filereptoolexample.md), Service: [FileRepServiceExample](filerepserviceexample.md).

## <a name="wcf-public-service-interoperation"></a>Interoperación de servicio público de WCF

Un cliente de servicios Web de Windows se comunica con un cliente de servicio de WCF: [WcfPublicServiceSample](wcfpublicservicesample.md).

## <a name="custom-http-proxy"></a>Proxy HTTP personalizado

Un cliente de servicios Web de Windows se comunica con un servicio ASMX TerraService mediante el cliente de proxy personalizado: [AsmxTerraServiceSampleWithCustomProxy](asmxterraservicesamplewithcustomproxy.md)

 

 




