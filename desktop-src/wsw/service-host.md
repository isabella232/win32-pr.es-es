---
title: Host de servicio
description: El host de servicio es el entorno en tiempo de ejecución para hospedar un servicio dentro de un proceso.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Servicios web host de servicio para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a09a41714ce80402c5430e6849988ae86163770af7ae3eb060fdd7925e861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838677"
---
# <a name="service-host"></a>Host de servicio

El host de servicio es el entorno en tiempo de ejecución para hospedar un servicio dentro de un proceso.


Un servicio puede configurar uno o varios puntos de conexión dentro de un host de servicio.

![Diagrama que muestra la estructura de un host de servicio que contiene un punto de conexión de servicio.](images/servicehost.png)

## <a name="creating-a-service-host"></a>Creación de un host de servicio

Antes de crear un host de servicio, un servicio debe definir sus puntos de conexión. Se especifica un punto de conexión en el host de servicio en la estructura [**WS \_ SERVICE \_ ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) y se define mediante la siguiente información:

-   Una dirección, que es el URI físico en el que se hospedará el servicio.
-   Estructura [**WS \_ CHANNEL \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) que especifica el tipo del canal subyacente para el punto de conexión.
-   Estructura [**WS \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) que especifica el enlace del canal.
-   Estructura [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que contiene la descripción de seguridad del punto de conexión.
-   Estructura [**WS \_ SERVICE \_ CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) que representa el [contrato de servicio](contract.md) para el punto de conexión.
-   Estructura [**WS \_ SERVICE SECURITY \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) que especifica una función de devolución de llamada de autorización para el punto de conexión.
-   Estructura [**WS \_ SERVICE ENDPOINT \_ \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) que contiene una matriz de propiedades de punto de conexión de servicio.

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

Solo se admiten contratos un-way para SOAP sobre UDP, representados por [**WS \_ UDP CHANNEL \_ \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) en la enumeración **\_ WS CHANNEL \_ BINDING.**

Una vez definido un punto de conexión, se puede pasar a la función [**WsCreateServiceHost,**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) que toma una matriz de punteros a las estructuras de punto de conexión [**de servicio \_ \_ de WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

Opcionalmente, una aplicación puede proporcionar una matriz de propiedades de [**servicio**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) a [**WsCreateServiceHost para**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) configurar opciones personalizadas en el host de servicio.

Una aplicación abre el host de servicio para empezar a aceptar solicitudes de cliente.

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

Después de abrir el host de servicio, la aplicación puede cerrarlo si no hay más operaciones que lo requieran. Tenga en cuenta que esto no libera sus recursos y que se puede volver a abrir con una llamada posterior a [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

Después de cerrar el host de servicio, una aplicación puede restablecer el host de servicio para su reutilización.

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

Cuando la aplicación se realiza con el host de servicio, puede liberar los recursos asociados al host de servicio mediante una llamada a la [**función WsFreeServiceHost.**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) Tenga en [**cuenta que se debe llamar a WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) antes de llamar a esta función.

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

Para obtener información sobre cómo adjuntar un estado personalizado al host de servicio, consulte [User Host State (Estado de host de usuario).](user-host-state.md)

Para obtener información sobre la autorización en un host de servicio para un punto de conexión determinado, vea [Autorización de servicio](service-authorization.md).

Para obtener información sobre la implementación de operaciones de servicio y contratos de servicio para un servicio, consulte los temas sobre operaciones [de](server-side-service-operations.md) servicio y [contrato de](contract.md)servicio.

## <a name="security"></a>Seguridad

Una aplicación puede usar las siguientes propiedades para controlar la cantidad de recursos que el host de servicio asigna en nombre de la aplicación:

-   [**WS \_ PROPIEDAD DE \_ PUNTO DE CONEXIÓN DE SERVICIO \_ \_ \_ ACEPTACIÓN MÁXIMA DE \_ CANALES**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_SIMULTANEIDAD \_ MÁXIMA DE LA PROPIEDAD DEL PUNTO DE CONEXIÓN DE \_ \_ SERVICIO**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)
-   [**WS \_ PROPIEDAD DE \_ PUNTO DE CONEXIÓN DE SERVICIO \_ \_ \_ CANALES MÁXIMOS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ TAMAÑO \_ MÁXIMO DEL MONTÓN DE MONTÓN DEL CUERPO DE LA PROPIEDAD DEL PUNTO DE CONEXIÓN \_ DE \_ \_ \_ \_ SERVICIO**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ TAMAÑO MÁXIMO DEL GRUPO DE LLAMADAS DE LA \_ PROPIEDAD DEL PUNTO DE CONEXIÓN DE \_ \_ \_ \_ \_ SERVICIO**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ TAMAÑO MÁXIMO \_ DEL \_ GRUPO DE \_ \_ \_ CANALES DE LA PROPIEDAD DEL PUNTO DE \_ CONEXIÓN DE SERVICIO.**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)

Se eligen valores predeterminados seguros para cada una de estas propiedades; una aplicación debe tener cuidado si desea modificar estas propiedades. Además de las propiedades mencionadas [](message.md) anteriormente, la aplicación también puede modificar [las](channel.md)propiedades [específicas](listener.md) del cliente de escucha y del mensaje. Consulte las consideraciones de seguridad de estos componentes antes de modificar cualquiera de estas opciones.

Además, las siguientes consideraciones de diseño de aplicaciones se deben evaluar cuidadosamente al usar la API de host de servicio WWSAPI:

-   Al usar MEX, las aplicaciones deben tener cuidado de no revelar datos confidenciales. Como mitigación, si la naturaleza de los datos que se exponen a través de MEX es confidencial, las aplicaciones pueden optar por configurar el punto de conexión MEX con un enlace seguro que requiera autenticación como mínimo e implementar la autorización como parte del punto de conexión mediante la devolución de llamada de seguridad del servicio [**WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   La propiedad FAULT DISCLOSURE de WS SERVICE PROPERTY deshabilita de forma predeterminada la información de error enriquecida a través de errores en el host [**\_ \_ \_ \_ de**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) servicio. Es decisión de la aplicación enviar información de error enriquección como parte del error. Sin embargo, esto puede dar lugar a la divulgación de información y, por lo tanto, se recomienda que esta configuración solo se cambie para escenarios de depuración.
-   Más allá de la validación realizada para Basic Profile 2.0 y la serialización XML, el host de servicio no realiza ninguna validación en el contenido de datos recibido como parte de los parámetros de la operación de servicio. Es responsabilidad de la aplicación realizar todas las validaciones de parámetros por sí misma.
-   La autorización no se implementa como parte del host de servicio. Sin embargo, las aplicaciones pueden implementar su propio esquema de autorización mediante [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) y [**WS \_ SERVICE SECURITY \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   Es responsabilidad de la aplicación usar enlaces seguros en su punto de conexión. El host de servicio no proporciona ninguna seguridad más allá de lo que se configura en el punto de conexión.

Los siguientes elementos de API se usan con el host de servicio.

| Devolución de llamada                                                                             | Descripción                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**WS \_ SERVICE \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | Se invoca cuando el host de servicio acepta un canal en un agente de escucha de punto de conexión. |
| [**DEVOLUCIÓN DE \_ LLAMADA DEL CANAL DE CIERRE DEL \_ \_ \_ SERVICIO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | Se invoca cuando se cierra o anula un canal en un punto de conexión.                     |



 



| Enumeración                                                                    | Descripción                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**IDENTIFICADOR DE PROPIEDAD \_ DEL PUNTO DE CONEXIÓN DE SERVICIO \_ \_ \_ DE WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | Parámetros opcionales para configurar un punto [**de conexión de servicio \_ de \_ WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) |
| [**ESTADO DEL \_ HOST DEL \_ SERVICIO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | Los estados en los que puede estar un host de servicio.                                                   |
| [**IDENTIFICADOR DE PROPIEDAD DEL SERVICIO WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | Parámetros opcionales para configurar el host de servicio.                                       |



 



| Función                                                     | Descripción                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | Interrumpe e interrumpe las operaciones actuales en el host de servicio.                          |
| [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | Cierra todos los agentes de escucha para que no se acepte ningún canal nuevo del cliente.                   |
| [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | Crea un host de servicio.                                                                      |
| [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | Libera la memoria asociada a un objeto de host de servicio.                                   |
| [**WsGetServiceHostProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | Recupera una propiedad de host de servicio especificada.                                                 |
| [**WsOpenServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | Abre un host de servicio para la comunicación e inicia los agentes de escucha en todos los puntos de conexión.        |
| [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | Restablece el host de servicio para su reutilización y restablece el canal subyacente y los agentes de escucha para su reutilización. |



 



| Handle                                       | Descripción                                      |
|----------------------------------------------|--------------------------------------------------|
| [**HOST DEL SERVICIO WS \_ \_**](ws-service-host.md) | Tipo opaco que se usa para hacer referencia a un host de servicio. |



 



| Estructura                                                                              | Descripción                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**PUNTO DE CONEXIÓN DE SERVICIO DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | Representa un punto de conexión individual en un host de servicio.                            |
| [**WS \_ SERVICE \_ ENDPOINT \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | Especifica una configuración específica del servicio.                                           |
| [**WS \_ SERVICE \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | Especifica una configuración específica del servicio.                                           |
| [**DEVOLUCIÓN DE \_ LLAMADA \_ DE ACEPTACIÓN DE LA PROPIEDAD \_ DEL \_ SERVICIO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | Especifica la devolución de llamada a la que se llama cuando se acepta correctamente un canal. |
| [**DEVOLUCIÓN DE \_ LLAMADA DE CIERRE DE PROPIEDAD DE SERVICIO \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | Especifica la devolución de llamada a la que se llama cuando un canal está a punto de cerrarse.    |



 

 

 




