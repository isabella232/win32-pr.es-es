---
title: Windows Ejemplos de servicios web
description: En los ejemplos siguientes se muestra cómo usar Windows API de servicios web.
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e38dd32923336f63d5d5195fbae8c4ee8a3c20ce2d5568b8f7557aba34f340
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109755"
---
# <a name="windows-web-services-examples"></a>Windows Ejemplos de servicios web

En los ejemplos siguientes se muestra cómo usar Windows API de servicios web.

-   [Ejemplos de modelos de servicio](service-model-examples.md)
-   [Ejemplos de capa de canal TCP](tcp-channel-layer-examples.md)
-   [Ejemplos de capa de canal HTTP](http-channel-layer-examples.md)
-   [Ejemplos de capa de canal UDP](udp-channel-layer-examples.md)
-   [Ejemplos de capas de canal de canalización con nombre](named-pipes-channel-layer-examples.md)
-   [Ejemplos de mensajes](message-examples.md)
-   [Ejemplos xml](xml-examples.md)
-   [Ejemplos de modelos asincrónicos](async-model-examples.md)
-   [Ejemplos de capa de canal de seguridad](security-channel-layer-examples.md)
-   [Ejemplos de replicación de archivos](file-replication-examples.md)

## <a name="service-model-examples"></a>Ejemplos de modelos de servicio

Servicio de calculadora: cliente: [HttpCalculatorClientExample](httpcalculatorclientexample.md), servidor: [HttpCalculatorServiceExample](httpcalculatorserviceexample.md).

Servicio de calculadora con seguridad de transporte SSL: cliente: [HttpCalculatorWithSslClientExample](httpcalculatorwithsslclientexample.md), servidor: [HttpCalculatorWithSslServiceExample](httpcalculatorwithsslserviceexample.md).

Servicio de calculadora con nombre de usuario sobre seguridad en modo mixto SSL: Cliente: [HttpCalculatorWithUsernameOverSslClientExample](httpcalculatorwithusernameoversslclientexample.md), Servidor: [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).

Servicio de calculadora con Kerberos sobre seguridad en modo mixto SSL: Cliente: [HttpCalculatorWithKerberosOverSslClientExample](httpcalculatorwithkerberosoversslclientexample.md), Servidor: [HttpCalculatorWithKerberosOverSslServiceExample](httpcalculatorwithkerberosoversslserviceexample.md).

Servicio de pedido de compra: [cliente: HttpPurchaseOrderClientExample](httppurchaseorderclientexample.md), servidor: [HttpPurchaseOrderServiceExample](httppurchaseorderserviceexample.md).

Servicio de pedido de compra con seguridad de transporte SSL: cliente: [HttpPurchaseOrderWithSslClientExample](httppurchaseorderwithsslclientexample.md), servidor: [HttpPurchaseOrderWithSslServiceExample](httppurchaseorderwithsslserviceexample.md).

Servicio de pedido de compra con nombre de usuario sobre seguridad en modo mixto SSL: Cliente: [HttpPurchaseOrderWithUsernameOverSslClientExample](httppurchaseorderwithusernameoversslclientexample.md), Servidor: [HttpPurchaseOrderWithUserNameOverSslServiceExample](httppurchaseorderwithusernameoversslserviceexample.md).

Servicio de pedido de compra con Kerberos a través de la seguridad en modo mixto ssl: Cliente: [HttpPurchaseOrderWithKerberosOverSslClientExample](httppurchaseorderwithkerberosoversslclientexample.md), Servidor: [HttpPurchaseOrderWithKerberosOverSslServiceExample](httppurchaseorderwithkerberosoversslserviceexample.md).

Servicio de pedido de compra sin tipo: Servidor: [UnTypedServiceExample](untypedserviceexample.md). Cliente: [UnTypedClientExample](untypedclientexample.md)

Calculadora con sesión: Servidor: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Cliente:[SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md).

Calculadora que usa un canal personalizado y una implementación de agente de escucha: Servidor:[HttpCalculatorWithLayeredChannelServiceExample](httpcalculatorwithlayeredchannelserviceexample.md). Cliente:[HttpCalculatorWithLayeredChannelClientExample](httpcalculatorwithlayeredchannelclientexample.md).

Calculadora que usa un canal codificado: Servidor:[HttpCalculatorWithEncodedChannelServiceExample](httpcalculatorwithencodedchannelserviceexample.md). Cliente:[HttpCalculatorWithEncodedChannelClientExample](httpcalculatorwithencodedchannelclientexample.md).

Servicio que controla solicitudes HTTP sin formato (no SOAP): Cliente:[HttpRawClientExample](httprawclientexample.md). Servidor:[HttpRawServiceExample](httprawserviceexample.md).

Notificación de anulación de la operación de servicio: [Servidor: BlockingServiceExample](blockingserviceexample.md). Cliente:[ServiceCancellationExample](servicecancellationexample.md).

Cancelación de llamadas: Servidor: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Cliente:[CallAbandoneExample](callabandonexample.md).

Cree manualmente una descripción de directiva y úsela para crear un proxy de servicio: [PolicyTemplateExample](policytemplateexample.md).

## <a name="tcp-channel-layer-examples"></a>Ejemplos de capa de canal TCP

Un ejemplo de TCP que envía mensajes mediante un patrón un solo sentido: Cliente: [OneWayTcpClientExample](onewaytcpclientexample.md), Servidor: [OneWayTcpServerExample](onewaytcpserverexample.md)

Un ejemplo de TCP que envía mensajes mediante un patrón de solicitud-respuesta: Client: [RequestReplyTcpClientExample](requestreplytcpclientexample.md), Server: [RequestReplyTcpServerExample](requestreplytcpserverexample.md)

Un ejemplo tcp de streaming: Cliente: [StreamingTcpClientExample](streamingtcpclientexample.md), Servidor: [StreamingTcpServerExample](streamingtcpserverexample.md)

Un ejemplo de TCP de streaming asincrónico: Cliente: [AsyncStreamingTcpClientExample](asyncstreamingtcpclientexample.md), Servidor: [AsyncStreamingTcpServerExample](asyncstreamingtcpserverexample.md)

## <a name="http-channel-layer-examples"></a>Ejemplos de capa de canal HTTP

Un ejemplo HTTP: Cliente: [HttpClientExample](httpclientexample.md), Servidor: [HttpServerExample](httpserverexample.md)

Un ejemplo HTTP que usa las API de streaming: Cliente: [StreamingHttpClientExample](streaminghttpclientexample.md), Servidor: [StreamingHttpServerExample](streaminghttpserverexample.md)

## <a name="udp-channel-layer-examples"></a>Ejemplos de capa de canal UDP

Un ejemplo de UDP que envía mensajes mediante un patrón unípido: [Cliente: OneWayUdpClientExample](onewayudpclientexample.md), Servidor: [OneWayUdpServerExample](onewayudpserverexample.md)

Un ejemplo de UDP que envía mensajes mediante un patrón de respuesta de solicitud de multidifusión: Cliente: [MulticastUdpClientExample](multicastudpclientexample.md), Servidor: [MulticastUdpServerExample](multicastudpserverexample.md) El siguiente es el mismo ejemplo, pero con direccionamiento IPv6: Cliente: [MulticastUdpClientExample6](multicastudpclientexample6.md), Servidor: [MulticastUdpServerExample6](multicastudpserverexample6.md)

## <a name="named-pipes-channel-layer-examples"></a>Ejemplos de capas de canal de canal con nombre

Ejemplo de canalizaciones con nombre que envía mensajes mediante un patrón de solicitud-respuesta: Client: [RequestReplyNamedPipesClientExample](requestreplynamedpipesclientexample.md), Server: [RequestReplyNamedPipesServerExample](requestreplynamedpipesserverexample.md)

Un ejemplo de canalizaciones con nombre de streaming: [Cliente: StreamingNamedPipesClientExample](streamingnamedpipesclientexample.md), Servidor: [StreamingNamedPipesServerExample](streamingnamedpipesserverexample.md)

## <a name="message-examples"></a>Ejemplos de mensajes

Un ejemplo que usa encabezados de mensaje personalizados: [CustomHeaderExample](customheaderexample.md)

Un ejemplo que codifica y descodifica un mensaje: [MessageEncodingExample](messageencodingexample.md)

Un ejemplo que reenvía un mensaje: [ForwardMessageExample](forwardmessageexample.md)

## <a name="xml-examples"></a>Ejemplos xml

Un ejemplo que escribe y lee xml mediante un búfer XML [ReadWriteXmlExample](readwritexmlexample.md)

Un ejemplo que escribe y lee datos binarios mediante MTOM, WsWriteBytes, WsPushBytes y WsPullBytes [ReadWriteBytesXmlExample](readwritebytesxmlexample.md)

Un ejemplo que navega por un búfer XML [NavigateXmlExample](navigatexmlexample.md)

Ejemplo que lee un nodo de documento XML por nodo [ReadXmlExample](readxmlexample.md)

Un ejemplo que busca y muestra un atributo XML [ReadAttributeExample](readattributeexample.md)

Un ejemplo que escribe y lee una matriz de elementos [ReadWriteArrayExample](readwritearrayexample.md)

Ejemplo que inserta un elemento en un búfer XML [InsertElementExample](insertelementexample.md)

Un ejemplo que muestra el uso de algunas funciones auxiliares de búfer XML [XmlBufferExample](xmlbufferexample.md)

Un ejemplo que escribe y lee el tipo derivado mediante funciones auxiliares generadas por wsutil [DerivedTypeExample](derivedtypeexample.md)

## <a name="async-model-examples"></a>Ejemplos de modelos asincrónicos

Ejemplo que muestra el modelo para las funciones asincrónicas. [AsyncModelExample](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a>Ejemplos de capa de canal de seguridad

Windows seguridad de transporte a través de TCP: Cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Servidor: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Windows seguridad de transporte a través de canalizaciones con nombre: Cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Servidor: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Seguridad de transporte SSL: cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nombre de usuario sobre seguridad en modo mixto SSL: Cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nombre de usuario sobre seguridad en modo mixto SSL: Cliente: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Servidor: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

## <a name="metadata-example"></a>Ejemplo de metadatos

En los ejemplos siguientes se muestra cómo procesar documentos WSDL y de directiva con el objetivo de extraer información sobre el protocolo que admite un punto de conexión.

Nombre de usuario sobre seguridad en modo mixto SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emitido sobre seguridad en modo mixto SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificado X509 sobre seguridad en modo mixto SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="ws-metadata-exchange-example"></a>WS-Metadata Exchange ejemplo

En los ejemplos siguientes se muestra cómo habilitar WS-MetadataExchange host [de servicio \_ \_ de WS](ws-service-host.md).

Servicio TCP con WS-MetadataExchange habilitado: [MetadataExchangeSample](metadataexchangesample.md). Cliente de moniker de servicio WCF que llama al servicio TCP WS-MetadataExchange habilitado: [ServiceMonikerSample](servicemonikersample.md).

## <a name="custom-headers-and-service-model"></a>Encabezados personalizados y modelo de servicio

En los ejemplos siguientes se muestra cómo usar encabezados personalizados con [WS \_ SERVICE \_ PROXY](ws-service-proxy.md) y [WS \_ SERVICE \_ HOST,](ws-service-host.md) respectivamente.

Cliente: [HttpCustomHeaderPurchaseOrderClientExample](httpcustomheaderpurchaseorderclientexample.md), Servidor: [HttpCustomHeaderPurchaseOrderServiceExample](httpcustomheaderpurchaseorderserviceexample.md).

## <a name="file-replication-sample"></a>Ejemplo de replicación de archivos

Un ejemplo completo que muestra cómo implementar un servicio de replicación de archivos: [Herramienta: FileRepToolExample](filereptoolexample.md), Servicio: [FileRepServiceExample](filerepserviceexample.md).

## <a name="wcf-public-service-interoperation"></a>Interoperación de servicios públicos de WCF

Un Windows web services se comunica con un cliente de servicio WCF: [WcfPublicServiceSample](wcfpublicservicesample.md).

## <a name="custom-http-proxy"></a>Proxy HTTP personalizado

Un Windows web services se comunica con un servicio ASMX TerraService mediante el cliente proxy personalizado: [AsmxServiceSampleWithCustomProxy](asmxterraservicesamplewithcustomproxy.md)

 

 




