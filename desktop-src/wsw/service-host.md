---
title: Host de servicio
description: El host de servicio es el entorno de tiempo de ejecución para hospedar un servicio dentro de un proceso.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Servicios Web de host de servicio para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105707515"
---
# <a name="service-host"></a>Host de servicio

El host de servicio es el entorno de tiempo de ejecución para hospedar un servicio dentro de un proceso.


Un servicio puede configurar uno o más puntos de conexión dentro de un host de servicio.

![Diagrama que muestra la estructura de un host de servicio que contiene un punto de conexión de servicio.](images/servicehost.png)

## <a name="creating-a-service-host"></a>Creación de un host de servicio

Antes de crear un host de servicio, un servicio debe definir sus extremos. Un punto de conexión en el host de servicio se especifica en la estructura de [**\_ punto de \_ conexión de servicio de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) y se define mediante la siguiente información:

-   Una dirección, que es el URI físico en el que se hospedará el servicio.
-   Estructura [**de \_ \_ tipo de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) que especifica el tipo del canal subyacente para el extremo.
-   Una estructura de [**\_ \_ enlace de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) que especifica el enlace del canal.
-   Una estructura de [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que contiene la descripción de seguridad para el extremo.
-   Estructura [**del \_ \_ contrato de servicio de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) que representa el contrato de [servicio](contract.md) para el extremo.
-   Una estructura de [**devolución de llamada de \_ seguridad del servicio \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) que especifica una función de devolución de llamada de autorización para el extremo.
-   Una estructura de [**\_ propiedad de punto de \_ conexión \_ de servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) que contiene una matriz de propiedades de punto de conexión de servicio.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

Solo se admiten contratos unidireccionales para SOAP a través de UDP, representado por el [**enlace de canal de WS \_ UDP \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) en la enumeración de **enlace de \_ canal \_ de WS** .

Una vez definido un punto de conexión, se puede pasar a la función [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , que toma una matriz de punteros a estructuras de punto de [**conexión de \_ servicio \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

Una aplicación puede proporcionar opcionalmente una matriz de [**propiedades de servicio**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) a [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) para configurar las opciones personalizadas en el host del servicio.

Una aplicación abre el host del servicio para iniciar la aceptación de solicitudes de cliente.

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

Después de abrir el host de servicio, la aplicación puede cerrarlo si no hay más operaciones que lo requieran. Tenga en cuenta que esto no libera sus recursos y que se puede volver a abrir con una llamada subsiguiente a [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

Después de cerrar el host de servicio, una aplicación puede restablecer el host de servicio para su reutilización.

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

Cuando la aplicación se realiza con el host de servicio, puede liberar los recursos asociados al host de servicio llamando a la función [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) . Tenga en cuenta que se debe llamar a [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) antes de llamar a esta función.

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

Para obtener información sobre cómo asociar un estado personalizado al host de servicio, consulte [Estado de host de usuario](user-host-state.md) .

Para obtener información sobre la autorización en un host de servicio para un punto de conexión determinado, consulte [autorización del servicio](service-authorization.md).

Para Iinformation sobre la implementación de operaciones de servicio y contratos de servicio para un servicio, consulte los temas sobre [operaciones](server-side-service-operations.md) de servicio y [contrato de servicio](contract.md).

## <a name="security"></a>Seguridad

Una aplicación puede usar las propiedades de seguimiento para controlar la cantidad de recursos que el host de servicio asigna en nombre de la aplicación:

-   [**WS \_ propiedad de punto de conexión de servicio \_ \_ \_ número máximo de \_ \_ canales de aceptación**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)
-   [**WS \_ propiedad de punto de conexión de servicio \_ \_ \_ Max \_ Concurrency**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ número máximo de \_ canales de propiedad de punto de conexión de servicio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)
-   [**WS \_ \_ \_ \_ \_ \_ \_ tamaño máximo del montón del cuerpo de la propiedad del extremo de servicio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ tamaño máximo del \_ grupo de \_ llamadas \_ de propiedad de punto de conexión de servicio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)
-   [**WS \_ \_ \_ \_ tamaño máximo de \_ grupo de \_ canales \_ de propiedad de punto de conexión de servicio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).

Se eligen los valores predeterminados seguros para cada una de estas propiedades. una aplicación debe tener cuidado si desea modificar estas propiedades. Además de las propiedades mencionadas anteriormente, la aplicación también puede modificar las propiedades específicas del [canal](channel.md), el [agente de escucha](listener.md) y el [mensaje](message.md) . Consulte las consideraciones de seguridad de estos componentes antes de modificar cualquiera de estos valores.

Además, las siguientes consideraciones sobre el diseño de la aplicación deben evaluarse cuidadosamente al usar la API del host del servicio WWSAPI:

-   Al usar MEX, las aplicaciones deben tener cuidado de no divulgar los datos confidenciales. Como medida de mitigación, si la naturaleza de los datos que se exponen a través de MEX es sensible, las aplicaciones pueden optar por configurar el punto de conexión MEX con un enlace seguro que requiera autenticación al menos e implementar la autorización como parte del punto de conexión mediante la [**devolución de llamada de \_ seguridad del servicio \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   De forma predeterminada, la información de error enriquecida a través de errores está deshabilitada en el host de servicio mediante la propiedad de divulgación de errores de la [**\_ propiedad de servicio \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) . Es el momento en que la aplicación envía información de error enriquecida como parte del error. Sin embargo, esto puede dar lugar a la divulgación de información y, por tanto, se recomienda que esta configuración solo se cambie para escenarios de depuración.
-   Además de la validación realizada para la serialización básica de perfiles 2,0 y XML, el host de servicio no realiza ninguna validación en el contenido de datos recibido como parte de los parámetros de operación de servicio. Es responsabilidad de la aplicación realizar todas las validaciones de parámetros por sí misma.
-   La autorización no se implementa como parte del host de servicio. Sin embargo, las aplicaciones pueden implementar su propio esquema de autorización mediante la [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) y la [**devolución de llamada de \_ \_ seguridad \_ del servicio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   Es responsabilidad de la aplicación usar enlaces seguros en su punto de conexión. El host de servicio no proporciona ninguna seguridad más allá de lo que se configura en el punto de conexión.

Los siguientes elementos de API se usan con el host de servicio.

| Devolución de llamada                                                                             | Descripción                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**servicio WS- \_ \_ devolución de \_ llamada de canal \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | Se invoca cuando el host de servicio acepta un canal en un agente de escucha del extremo. |
| [**\_devolución de \_ llamada de canal de cierre de servicio WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | Se invoca cuando se cierra o se anula un canal en un extremo.                     |



 



| Enumeración                                                                    | Descripción                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**identificador de la \_ propiedad de punto de conexión de servicio WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | Parámetros opcionales para configurar un [**\_ punto de \_ conexión de servicio de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint). |
| [**\_Estado de \_ host de servicio WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | Los Estados en los que puede estar un host de servicio.                                                   |
| [**identificador de la \_ propiedad de servicio WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | Parámetros opcionales para configurar el host de servicio.                                       |



 



| Función                                                     | Descripción                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | Interrumpe y suspende las operaciones actuales en el host de servicio.                          |
| [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | Cierra todos los agentes de escucha para que no se acepte ningún canal nuevo desde el cliente.                   |
| [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | Crea un host de servicio.                                                                      |
| [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | Libera la memoria asociada a un objeto host de servicio.                                   |
| [**WsGetServiceHostProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | Recupera una propiedad de host de servicio especificada.                                                 |
| [**WsOpenServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | Abre un host de servicio para la comunicación e inicia los agentes de escucha en todos los extremos.        |
| [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | Restablece el host de servicio para reutilizarlo y restablece el canal subyacente y los agentes de escucha para su reutilización. |



 



| Handle                                       | Descripción                                      |
|----------------------------------------------|--------------------------------------------------|
| [**\_host de servicio WS \_**](ws-service-host.md) | Tipo opaco que se usa para hacer referencia a un host de servicio. |



 



| Estructura                                                                              | Descripción                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_extremo de servicio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | Representa un punto de conexión individual en un host de servicio.                            |
| [**\_propiedad de \_ punto de conexión de servicio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | Especifica una configuración específica del servicio.                                           |
| [**\_propiedad de servicio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | Especifica una configuración específica del servicio.                                           |
| [**devolución de llamada de la \_ \_ propiedad de servicio WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | Especifica la devolución de llamada a la que se llama cuando un canal se acepta correctamente. |
| [**\_devolución de \_ llamada de cierre de propiedad de servicio WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | Especifica la devolución de llamada a la que se llama cuando un canal está a punto de cerrarse.    |



 

 

 




