---
title: Crear manualmente un proxy de servicio para un servicio WCF
description: La forma más fácil de crear un proxy de servicio de cliente para un servicio de Windows Communication Foundation (WCF) es la capa de modelo de servicio con la herramienta WsUtil, como se describe en el tema crear un cliente.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e061fda95298986ee6336dee0662d80c89a0a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695376"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Crear manualmente un proxy de servicio para un servicio WCF

La forma más fácil de crear un proxy de servicio de cliente para un servicio de Windows Communication Foundation (WCF) es la capa de [modelo de servicio](service-model-layer-overview.md) con la herramienta WsUtil, como se describe en el tema [crear un cliente](creating-a-client.md) . Sin embargo, si es necesario, también puede crear manualmente un proxy de servicio. Esta API incluye una función [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) para crear el proxy de servicio, así como estructuras, enumeraciones, etc. para establecer las propiedades necesarias para interoperar con WCF.

WCF proporciona una serie de enlaces estándar y cada uno de ellos tiene como destino un escenario de uso específico. El enlace que utiliza el servicio al que intenta conectarse, a su vez, determina qué propiedades de canal se deben personalizar para que el proxy de servicio se comunique con el servicio.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Creación de un proxy de servicio para WSHttpBinding de WCF

WSHttpBinding es para el escenario principal de servicios Web de Internet. Usa la versión de SOAP 1,2 y WS-Addressing versión 1,0 más recientes y habilita una amplia gama de opciones de seguridad en los transportes HTTP y HTTPS públicos. WWSAPI no tiene un equivalente de WSHttpBinding (o cualquiera de los enlaces estándar de WCF, en ese caso), pero como su versión predeterminada de SOAP, WS-Addressing versión y el formato de codificación coinciden con los de WSHttpBinding, la creación de un proxy de servicio para un servicio que usa WSHttpBinding es sencilla. Por ejemplo, para crear un proxy de servicio para comunicarse con un punto de conexión WSHttpBinding sin seguridad, puede usar simplemente código como el fragmento de código siguiente (declaración de variables, y se omite la creación de montones y errores). Observe que no se ha especificado ninguna propiedad de canal ni Descripción de seguridad en la llamada a la función [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .


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

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Creación de un proxy de servicio para BasicHttpBinding de WCF

Sin embargo, al crear manualmente un proxy de servicio para un servicio WCF que utiliza un enlace BasicHttpBinding, es necesario establecer la versión de SOAP y WS-Addressing las propiedades del canal. Esto se debe a que el valor predeterminado de WWSAPI es SOAP versión 1,2 y WS-Addressing 1,0. El BasicHttpBinding de WCF, por otro lado, usa la versión 1,1 de SOAP y no WS-Addressing.

Para establecer la versión de SOAP y WS-Addrssing las propiedades del canal, declare una matriz de estructuras de [**\_ \_ propiedades de canal de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) para que contenga las propiedades de canal y la información relacionada.


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



A continuación, pase la matriz de propiedades de canal (channelProperties) y el recuento de propiedades (channelPropertyCount) a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (o [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) si está trabajando en la capa de canal).


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



La matriz que declaró para contener las propiedades se copia en **WsCreateServiceProxy** y, como resultado, puede liberar la memoria de la matriz de propiedades inmediatamente después de llamar a la función. Además, si asigna la memoria de la pila (como el fragmento de código anterior), también puede devolver desde la función inmediatamente después de la llamada.

## <a name="other-bindings"></a>Otros enlaces

Además, WWSAPI proporciona mecanismos para crear proxies de servicio para comunicarse con los servicios WCF mediante otros enlaces, como NetTcpBinding y WSFederationHttpBinding. Muchos de estos enlaces requieren el establecimiento de propiedades adicionales del canal, como descriptores de seguridad. Para obtener ejemplos que ilustran el uso de otros enlaces, consulte la sección ejemplos de [servicios Web de Windows](windows-web-services-examples.md), en concreto los ejemplos de capas de canales [TCP](tcp-channel-layer-examples.md), ejemplos de [capas de canales http](http-channel-layer-examples.md)y [ejemplos de capas](security-channel-layer-examples.md) de canales de seguridad.

 

 




