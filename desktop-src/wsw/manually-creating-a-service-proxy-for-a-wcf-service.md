---
title: Crear manualmente un proxy de servicio para un servicio WCF
description: La manera más fácil de crear un proxy de servicio de cliente para un servicio Windows Communication Foundation (WCF) es en el nivel de modelo de servicio con la herramienta WsUtil, como se describe en el tema Creación de un cliente.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33133ae48dee89e72871712d445453e237116f6f1fa08cf66a76381ea8d3d424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927255"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Crear manualmente un proxy de servicio para un servicio WCF

La manera más fácil de crear un proxy de servicio de cliente [](service-model-layer-overview.md) para un servicio Windows Communication Foundation (WCF) es en el nivel de modelo de servicio con la herramienta WsUtil, como se describe en el tema Creación de un cliente. [](creating-a-client.md) Sin embargo, si es necesario, también puede crear manualmente un proxy de servicio. Esta API incluye una función [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) para crear el proxy de servicio, así como estructuras, enumeraciones, y así sucesivamente para establecer las propiedades necesarias para interoperar con WCF.

WCF proporciona una serie de enlaces estándar, cada uno de los que tienen como destino un escenario de uso específico. A su vez, el enlace al servicio al que está intentando conectarse determina qué propiedades de canal debe personalizar para que el proxy de servicio se comunique con el servicio.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Crear un proxy de servicio para WSHttpBinding de WCF

WSHttpBinding es para el escenario de servicios web de Internet de línea principal. Usa las versiones soap 1.2 y WS-Addressing 1.0 más recientes y habilita una amplia gama de configuraciones de seguridad en los transportes HTTP y HTTPS públicos. WWSAPI no tiene un equivalente de WSHttpBinding (o cualquiera de los enlaces estándar de WCF, en ese caso), pero como su versión predeterminada de SOAP, versión WS-Addressing y formato de codificación coinciden con los de WSHttpBinding, la creación de un proxy de servicio para un servicio que usa WSHttpBinding es sencilla. Por ejemplo, para crear un proxy de servicio para hablar con un punto de conexión WSHttpBinding sin seguridad, simplemente puede usar código como el siguiente fragmento de código (declaración de variable y se omite la creación del montón y el error). Observe que no se especifica ninguna descripción de seguridad ni propiedades de canal en la llamada a la [**función WsCreateServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)


```C++
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        NULL, // channel properties
        0, // channel property count
        &proxy, 
        error);
```



La función crea el proxy de servicio y devuelve un puntero a él en el parámetro *serviceProxy* (&proxy en la llamada de función anterior).

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Crear un proxy de servicio para BasicHttpBinding de WCF

Sin embargo, cuando se crea manualmente un proxy de servicio para un servicio WCF que usa un enlace BasicHttpBinding, es necesario establecer la versión soap y WS-Addressing propiedades del canal. Esto se debe a que WWSAPI tiene como valor predeterminado SOAP versión 1.2 y WS-Addressing 1.0. Por otro lado, BasicHttpBinding de WCF usa la versión 1.1 de SOAP y no WS-Addressing.

Para establecer la versión soap WS-Addrssing propiedades del canal, declare una matriz de estructuras [**\_ CHANNEL \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) de WS para contener las propiedades del canal y la información relacionada.


```
WS_CHANNEL_PROPERTY channelProperties[4]; // Array to hold up to 4 channel properties

ULONG channelPropertyCount = 0; // Count of properties set
 
WS_ENVELOPE_VERSION soapVersion = WS_ENVELOPE_VERSION_SOAP_1_1; // Set required SOAP version
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ENVELOPE_VERSION; // Type of first channel property
channelProperties[channelPropertyCount].value = &soapVersion; // Address of the SOAP version value
channelProperties[channelPropertyCount].valueSize = sizeof(soapVersion); // Size of the value
channelPropertyCount++; // Increment property count
 
WS_ADDRESSING_VERSION addressingVersion = WS_ADDRESSING_VERSION_TRANSPORT; // Set required WS-Addressing value
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ADDRESSING_VERSION; // Type of second channel property
channelProperties[channelPropertyCount].value = &addressingVersion ; // Address of the WS-Addressing value
channelProperties[channelPropertyCount].valueSize = sizeof(addressingVersion ); // Size of the value
channelPropertyCount++; // Increment property count
 
// add more channel properties here

```



A continuación, pase la matriz de propiedades de canal (channelProperties) y el recuento de propiedades (channelPropertyCount) a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (o [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) si está trabajando en el nivel de canal).


```
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        channelProperties, // channel properties
        channelPropertyCount, // channel property count
        &proxy, 
        error);
```



La matriz declarada para contener las propiedades se copia en **WsCreateServiceProxy** y, como resultado, puede liberar la memoria de la matriz de propiedades inmediatamente después de llamar a la función. Además, si asigna la memoria de la pila (como el fragmento de código anterior), también puede volver de la función inmediatamente después de la llamada.

## <a name="other-bindings"></a>Otros enlaces

Además, WWSAPI proporciona mecanismos para crear servidores proxy de servicio para comunicarse con servicios WCF mediante otros enlaces, como NetTcpBinding y WSFederationHttpBinding. Muchos de estos enlaces requieren establecer propiedades de canal adicionales, como descriptores de seguridad. Para obtener ejemplos que ilustran el uso de otros enlaces, vea la sección Ejemplos de servicios web de [Windows](windows-web-services-examples.md), en particular los ejemplos de capa de canal [TCP,](tcp-channel-layer-examples.md)los ejemplos de capa de canal [HTTP](http-channel-layer-examples.md)y las [subsecciones](security-channel-layer-examples.md) Ejemplos de capa de canal de seguridad.

 

 




