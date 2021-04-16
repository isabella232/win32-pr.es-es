---
title: Configurar propiedades
description: Configurar propiedades
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f898467f92f669596b4a8b1a4e68581c343ea883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418675"
---
# <a name="configuring-properties"></a>Configurar propiedades

La API del servidor HTTP versión 2,0 permite a las aplicaciones configurar manualmente colas de solicitudes, sesiones de servidor y grupos de direcciones URL. La sesión de servidor es el objeto de nivel superior que contiene la información de configuración que se aplica a todos los grupos de direcciones URL creados en ellos. La aplicación crea una sesión de servidor con uno o más grupos de direcciones URL en ella y, a continuación, asocia el grupo de direcciones URL a una cola de solicitudes.

Para obtener más información acerca de los objetos de configuración específicos de la API del servidor HTTP versión 2,0, consulte:

-   [Configurar la sesión de servidor](configuring-the-server-session.md)
-   [Configuración del grupo de direcciones URL](configuring-the-url-group.md)
-   [Configuración de los temporizadores de gran nivel de API de servidor HTTP](configuring-the-http-server-api-wide-timers.md)

Las propiedades de los objetos de configuración se establecen con [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty), [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) y [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) , tal y como se muestra en el diagrama siguiente. La asociación entre la cola de solicitudes y el grupo de direcciones URL se puede cambiar a petición, mientras que no se puede cambiar la asociación entre la sesión del servidor y los grupos de direcciones URL. Los grupos de direcciones URL deben estar asociados a una cola de solicitudes para recibir solicitudes.

![propiedades de los objetos de configuración](images/configpropinv2.png)

En la tabla siguiente se enumeran las propiedades que se pueden establecer en cada objeto de configuración. En general, si la aplicación no establece ninguna configuración de propiedades, se aplican las configuraciones predeterminadas de la API del servidor HTTP. Las propiedades de configuración establecidas por la aplicación en la sesión de servidor invalidan las configuraciones de toda la API del servidor HTTP. Las configuraciones establecidas en el grupo de direcciones URL invalidan las configuraciones de sesión del servidor y las configuraciones de la cola de solicitudes invalidan las configuraciones predeterminadas de la API del servidor HTTP.



| Objeto Configuration | Propiedad                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sesión de servidor       | HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty                           |
| Grupo de direcciones URL            | HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty |
| Cola de solicitudes        | HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty                                                                          |



 

Las propiedades de la sesión del servidor se definen en la enumeración de la [ \_ \_ propiedad del servidor http](/windows/desktop/api/Http/ne-http-http_server_property) . En la tabla siguiente se enumeran las estructuras de propiedades que se establecen para cada tipo de propiedad y la API del servidor HTTP predeterminada cuando la aplicación no establece estas propiedades.



| Propiedad                                                    | Estructura                                                                     | HTTP Server API predeterminada    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| HttpServerAuthenticatonProperty                             | [**\_información de \_ autenticación del servidor HTTP \_**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | Sin autenticación          |
| HttpServerLoggingProperty                                   | [**\_información de registro http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)                              | Sin registro                 |
| HttpServerQosProperty->HttpQosSettingTypeConnectionLimit | [**\_información de \_ límite de conexión HTTP \_**](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | Ilimitado                   |
| HttpServerTimeoutsProperty                                  | [**información de límite de tiempo de \_ espera http \_ \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | 120 s.                   |
| HttpServerQosProperty->HttpQosSettingTypeBandwidth       | [**información de límite de ancho de \_ banda http \_ \_**](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | Ilimitado                   |
| HttpServerQueueLengthProperty                               | ULONG                                                                         | 1000                       |
| HttpServerStateProperty                                     | [**\_información de estado de http \_**](/windows/desktop/api/Http/ns-http-http_state_info)                                  | habilitado                    |
| HttpServer503VerbosityProperty                              | [**Nivel \_ de \_ detalle de respuesta http 503 \_**](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | HttpResponseVerbosityBasic |
| HttpServerBindingProperty                                   | [**\_información de enlace http \_**](/windows/desktop/api/Http/ns-http-http_binding_info)                              | None                       |



 

En la tabla siguiente se enumeran los valores mínimo y máximo de las configuraciones de la API del servidor HTTP.



| Propiedad                                              | API del servidor HTTP máximo y mínimo                        |
|-------------------------------------------------------|------------------------------------------------------------|
| HttpServerQosProperty->HttpQosSettingTypeBandwidth | Min = límite mínimo de \_ \_ ancho de banda permitido máx. \_ \_ = ninguno |
| HttpServerQueueLengthProperty                         | Min = 0xA Max = 0xFFFF                                     |



 

 

 




