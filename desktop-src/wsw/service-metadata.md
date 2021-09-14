---
title: Metadatos de servicio
description: El host de servicio WWSAPI admite WS-MetadataExchange para sus puntos de conexión.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Servicios web nativos de metadatos de servicio
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360573"
---
# <a name="service-metadata"></a>Metadatos de servicio

El host de servicio WWSAPI admite WS-MetadataExchange para sus puntos de conexión. Habilite este intercambio de metadatos en el host de servicio con los pasos siguientes:

-   Especifique los documentos de metadatos [**en la propiedad WS SERVICE \_ \_ METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) en [el \_ \_ host de WS SERVICE](ws-service-host.md).
-   Especifique el nombre del servicio en la [**propiedad WS \_ SERVICE \_ METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) en el host de servicio de [WS \_ \_](ws-service-host.md).
-   Especifique el puerto para los puntos de conexión individuales mediante la propiedad [**WS \_ SERVICE ENDPOINT PROPERTY \_ \_ \_ METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) en [**WS SERVICE \_ \_ ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).
-   Habilite una o varias estructuras de punto de conexión de servicio de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) para dar servicio a WS-MetadataExchange solicitudes.
-   Opcionalmente, especifique **WS \_ SERVICE ENDPOINT PROPERTY METADATA EXCHANGE URL \_ \_ \_ \_ \_ \_ SUFFIX** en la enumeración [**WS SERVICE ENDPOINT PROPERTY \_ \_ \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) para atender Ws-MetadataExchange solicitudes en una dirección específica.


Especificación de documentos de metadatos o nombre de servicio en el host de servicio

El primer paso es especificar los documentos de metadatos en el host de servicio. Para ello, resalte los documentos individuales como una matriz de cadenas \_ XML de WS. \_ \* Estas cadenas pueden ser esquema XML, WSDL o WS-Policy documento. Esto se especifica a través de la [**propiedad WS \_ SERVICE PROPERTY \_ \_ METADATA.**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)

Opcionalmente, una aplicación también puede especificar el nombre del servicio y el espacio de nombres como parte de [**WS \_ SERVICE \_ METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata). Si el documento de metadatos no especifica el elemento de servicio para el nombre de servicio especificado, el modelo de servicio generará un elemento de servicio con los puertos WSDL correspondientes para el servicio.

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

Tenga en cuenta que no se realizará ninguna comprobación de los documentos de metadatos individuales en los documentos. Es responsabilidad de la aplicación validar el contenido de los documentos y asegurarse de que todas las rutas de acceso de importación están relativamente especificadas.

El espacio de nombres especificado se usa para buscar el documento en el que el host de servicio agregará el elemento de servicio.

Adición del elemento de servicio al documento WSDL

El host de servicio proporciona la facilidad para que la aplicación agregue un elemento de servicio en su nombre si aún no se ha especificado uno. Para habilitar este comportamiento, una aplicación debe especificar los campos serivceName y serviceNs en la estructura [**WS \_ SERVICE \_ METADATA.**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) Si serviceName y serviceNs son **NULL,** no se agrega ningún elemento de servicio al documento WSDL. Ambos se usan para identificar el documento en el que se va a agregar serviceElement.

Si [**no se especifica la propiedad \_ WS SERVICE PROPERTY \_ \_ METADATA,**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) no se llevará a cabo ninguna excepción de metadatos en el host de servicio.

Especificación del puerto en el punto de conexión de servicio de WS \_ \_

Para que un punto de conexión de servicio de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) esté disponible como puerto dentro del elemento de servicio en el documento WSDL, la aplicación debe especificar en él la propiedad [**WS \_ SERVICE ENDPOINT \_ PROPERTY \_ \_ METADATA.**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)

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

Se supone que la referencia al nombre de enlace y al espacio de nombres existe en los documentos especificados en el host de servicio como parte de WS \_ SERVICE \_ PROPERTY \_ METADATA. El tiempo de ejecución no lo comprueba en nombre de la aplicación.

Habilitación WS-MetadataExchange servicio en el punto de conexión de servicio de WS \_ \_

Para atender las solicitudes WS-MetadataExchange servicio, el host de servicio debe tener al menos un punto de conexión habilitado para el mantenimiento WS-MetadataExchange solicitudes. Para ello, se establece la versión adecuada para WS-MetadataExchange en el punto de [**conexión de servicio de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Habilitación del servicio HTTP GET en WS \_ SERVICE \_ ENDPOINT

Para atender las solicitudes GET HTTP, el host de servicio debe tener al menos un punto de conexión habilitado para atender WS-MetadataExchange solicitudes. Para ello, se establece la versión adecuada para WS-MetadataExchange en el punto de [**conexión de servicio de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Especificación del sufijo de dirección URL Ws-MetadataExchange solicitudes

Opcionalmente, una aplicación solo puede habilitar la aceptación de solicitudes WS-MetadataExchange en una ruta de acceso específica. Para ello, especifique un sufijo para el punto de conexión de servicio de WS \_ \_ determinado. Este sufijo se concatena tal como está en la dirección URL real del punto de conexión de servicio \_ de WS. \_ La cadena concatenada se usa como dirección URL correspondiente al encabezado "to" recibido.

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

Los siguientes elementos de API se relacionan con la metada de servicio.

| Enumeración                                                       | Descripción                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**WS \_ METADATA \_ EXCHANGE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | Habilita o deshabilita el WS-MetadataExchange y HTTP GET en el punto de conexión. |



 



| Estructura                                                               | Descripción                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**METADATOS DEL \_ PUNTO DE CONEXIÓN DE \_ SERVICIO DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | Representa el elemento port para el punto de conexión.                         |
| [**METADATOS DEL SERVICIO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | Especifica la matriz de documentos de metadatos de servicio.                       |
| [**DOCUMENTO DE METADATOS \_ \_ DEL SERVICIO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | Especifica los documentos individuales que son los metadatos del servicio. |



 

 

 




