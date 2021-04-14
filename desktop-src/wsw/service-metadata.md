---
title: Metadatos de servicio
description: El host de servicio WWSAPI admite WS-MetadataExchange para sus extremos.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Metadatos de servicio nativos-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488567"
---
# <a name="service-metadata"></a>Metadatos de servicio

El host de servicio WWSAPI admite WS-MetadataExchange para sus extremos. Habilite este intercambio de metadatos en el host de servicio con los pasos siguientes:

-   Especifique los documentos de metadatos en la propiedad de [**\_ \_ metadatos del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) en el [ \_ \_ host del servicio WS](ws-service-host.md).
-   Especifique el nombre del servicio en la propiedad de [**\_ \_ metadatos del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) en el [ \_ \_ host del servicio WS](ws-service-host.md).
-   Especifique el puerto para los puntos de conexión individuales mediante la propiedad de [**\_ \_ \_ \_ metadatos de la propiedad de punto de conexión de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) en el [**\_ \_ extremo del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).
-   Habilite una o varias estructuras de [**\_ \_ extremos de servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) para atender las solicitudes de WS-MetadataExchange.
-   Opcionalmente, especifique el sufijo de la **\_ \_ \_ \_ \_ \_ dirección URL de \_ intercambio de metadatos de la propiedad de punto de conexión de WS Service** en la enumeración identificador de la [**\_ \_ \_ propiedad \_ de punto de conexión de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) para atender solicitudes Ws-MetadataExchange en una dirección


Especificación de documentos de metadatos/nombre de servicio en el host de servicio

El primer paso es especificar los documentos de metadatos en el host de servicio. Para ello, recopile los documentos individuales como una matriz de las \_ cadenas XML de WS \_ \* . Estas cadenas pueden ser esquemas XML, WSDL o WS-Policy documento. Esto se especifica mediante la [**propiedad \_ \_ \_ metadatos de la propiedad de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .

Opcionalmente, una aplicación también puede especificar el nombre del servicio y el espacio de nombres como parte de los [**\_ \_ metadatos del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata). Si el documento de metadatos no especifica el elemento de servicio para el nombre de servicio determinado, el modelo de servicio generará un elemento de servicio con los puertos WSDL correspondientes para el servicio.

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

Tenga en cuenta que no se realizará ninguna comprobación de los documentos de metadatos individuales en los documentos. Es responsabilidad de la aplicación validar el contenido de los documentos y asegurarse de que todas las rutas de acceso de las importaciones se especifican de forma relativa.

El espacio de nombres especificado se utiliza para buscar el documento en el que el host de servicio agregará el elemento de servicio.

Adición del elemento de servicio al documento WSDL

El host de servicio proporciona el recurso para que la aplicación agregue un elemento de servicio en su nombre si aún no se ha especificado ninguno. Para habilitar este comportamiento, una aplicación debe especificar los campos serivceName y servicens en la estructura de [**\_ \_ metadatos del servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) . Si serviceName y servicens son **null** , no se agrega ningún elemento de servicio al documento WSDL. Ambos se usan para identificar el documento en el que se va a agregar el serviceElement.

Si no se especifica la propiedad de [**\_ \_ \_ metadatos de la propiedad de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) , no se producirá ningún metadato en el host de servicio.

Especificar el puerto en el extremo del \_ servicio \_ WS

Para que [**un \_ punto de \_ conexión de servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) esté disponible como un puerto dentro del elemento de servicio en el documento WSDL, la aplicación debe especificar en él la propiedad de [**\_ \_ \_ \_ metadatos de la propiedad de punto de conexión de servicio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

Se supone que la referencia al nombre de enlace y espacio de nombres existe en los documentos especificados en el host de servicio como parte de los metadatos de la propiedad de servicio de WS \_ \_ \_ . El tiempo de ejecución no lo comprueba en nombre de la aplicación.

Habilitar el servicio de WS-MetadataExchange en el punto de conexión de \_ servicio WS \_

Para atender las solicitudes de WS-MetadataExchange, el host del servicio debe tener al menos un punto de conexión habilitado para atender las solicitudes de WS-MetadataExchange. Esto se hace estableciendo la versión adecuada para WS-MetadataExchange en el [**extremo del \_ servicio \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Habilitar el servicio GET de HTTP en el punto de conexión de \_ servicio WS \_

Para serviceHTTP solicitudes GET, el host del servicio debe tener al menos un punto de conexión habilitado para atender las solicitudes de WS-MetadataExchange. Esto se hace estableciendo la versión adecuada para WS-MetadataExchange en el [**extremo del \_ servicio \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Especificar el sufijo de dirección URL para solicitudes de Ws-MetadataExchange

Opcionalmente, una aplicación puede habilitar solo aceptar solicitudes de WS-MetadataExchange en una ruta de acceso específica. Esto se hace especificando un sufijo para el punto de conexión de servicio de WS determinado \_ \_ . Este sufijo se concatena tal cual con la dirección URL real del punto de conexión de servicio de WS \_ \_ . La cadena concatenada se utiliza como la dirección URL correspondiente al encabezado ' to ' recibido.

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

Los siguientes elementos de la API se relacionan con el servicio basan.

| Enumeración                                                       | Descripción                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_tipo de intercambio de metadatos de WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | Habilita o deshabilita WS-MetadataExchange y el servicio GET de HTTP en el punto de conexión. |



 



| Estructura                                                               | Descripción                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**metadatos de \_ punto de conexión de servicio WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | Representa el elemento Port para el extremo.                         |
| [**metadatos del \_ servicio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | Especifica la matriz de documentos de metadatos de servicio.                       |
| [**\_documento de \_ metadatos del servicio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | Especifica los documentos individuales que componen los metadatos del servicio. |



 

 

 




