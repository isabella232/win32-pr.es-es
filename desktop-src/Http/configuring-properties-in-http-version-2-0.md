---
title: Configuración de propiedades
description: Configuración de propiedades
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681d5707840634f86da41d3e67a1014e93b8450c668cae9ea6f3129a0fe021f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047464"
---
# <a name="configuring-properties"></a>Configuración de propiedades

La API del servidor HTTP versión 2.0 permite a las aplicaciones configurar manualmente colas de solicitudes, sesiones de servidor y grupos de direcciones URL. La sesión de servidor es el objeto de nivel superior que contiene información de configuración que se aplica a todos los grupos de direcciones URL creados en ellos. La aplicación crea una sesión de servidor con uno o varios grupos de direcciones URL en ella y, a continuación, asocia el grupo de direcciones URL a una cola de solicitudes.

Para obtener más información sobre objetos de configuración específicos en la API de servidor HTTP versión 2.0, consulte:

-   [Configuración de la sesión de servidor](configuring-the-server-session.md)
-   [Configuración del grupo de direcciones URL](configuring-the-url-group.md)
-   [Configuración de los temporizadores anchos de LA API del servidor HTTP](configuring-the-http-server-api-wide-timers.md)

Las propiedades de los objetos de configuración se establecen con [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty), [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) y [**HttpSetRequestQueueProperty,**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) como se muestra en el diagrama siguiente. La asociación entre la cola de solicitudes y el grupo de direcciones URL se puede cambiar a petición, mientras que la asociación entre la sesión del servidor y los grupos de direcciones URL no se puede cambiar. Los grupos de direcciones URL deben estar asociados a una cola de solicitudes para recibir solicitudes.

![propiedades de los objetos de configuración](images/configpropinv2.png)

En la tabla siguiente se enumeran las propiedades que se pueden establecer en cada objeto de configuración. En general, si la aplicación no establece ninguna configuración de propiedades, se aplican las configuraciones predeterminadas de la API del servidor HTTP. Las propiedades de configuración establecidas por la aplicación en la sesión del servidor invalidan las configuraciones de toda la API del servidor HTTP. Las configuraciones establecidas en el grupo de direcciones URL invalidan las configuraciones de sesión de servidor y las configuraciones de cola de solicitudes invalidan las configuraciones predeterminadas de la API del servidor HTTP.



| Objeto Configuration | Propiedad                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sesión de servidor       | HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty                           |
| Grupo de direcciones URL            | HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty |
| Cola de solicitudes        | HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty                                                                          |



 

Las propiedades de sesión del servidor se definen en la [enumeración HTTP \_ SERVER \_ PROPERTY.](/windows/desktop/api/Http/ne-http-http_server_property) En la tabla siguiente se enumeran las estructuras de propiedad que se establecen para cada tipo de propiedad y el valor predeterminado de la API del servidor HTTP cuando la aplicación no establece estas propiedades.



| Propiedad                                                    | Estructura                                                                     | Valor predeterminado de LA API del servidor HTTP    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| HttpServerAuthenticatonProperty                             | [**INFORMACIÓN \_ DE \_ AUTENTICACIÓN DEL SERVIDOR \_ HTTP**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | Sin autenticación          |
| HttpServerLoggingProperty                                   | [**INFORMACIÓN \_ DE REGISTRO \_ HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info)                              | Sin registro                 |
| HttpServerQosProperty->HttpQosSettingTypeConnectionLimit | [**INFORMACIÓN \_ DEL LÍMITE DE CONEXIÓN \_ \_ HTTP**](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | Ilimitado                   |
| HttpServerTimeoutsProperty                                  | [**INFORMACIÓN DEL \_ LÍMITE DE TIEMPO DE ESPERA \_ \_ DE HTTP**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | 120 s.                   |
| HttpServerQosProperty->HttpQosSettingTypeBandwidth       | [**INFORMACIÓN DEL \_ LÍMITE DE ANCHO DE BANDA \_ \_ HTTP**](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | Ilimitado                   |
| HttpServerQueueLengthProperty                               | ULONG                                                                         | 1000                       |
| HttpServerStateProperty                                     | [**INFORMACIÓN \_ DE ESTADO \_ HTTP**](/windows/desktop/api/Http/ns-http-http_state_info)                                  | habilitado                    |
| HttpServer503VerbosityProperty                              | [**DETALLE DE LA RESPUESTA HTTP \_ 503 \_ \_**](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | HttpResponseVerbosityBasic |
| HttpServerBindingProperty                                   | [**INFORMACIÓN \_ DE ENLACE \_ HTTP**](/windows/desktop/api/Http/ns-http-http_binding_info)                              | Ninguno                       |



 

En la tabla siguiente se enumeran los valores mínimo y máximo para las configuraciones de LA API del servidor HTTP.



| Propiedad                                              | Máximo y mínimo de LA API del servidor HTTP                        |
|-------------------------------------------------------|------------------------------------------------------------|
| HttpServerQosProperty->HttpQosSettingTypeBandwidth | Min = MIN \_ ALLOWED \_ BANDWIDTH \_ THROTTLING \_ RATE Max = none |
| HttpServerQueueLengthProperty                         | Min = 0xA Max = 0xFFFF                                     |



 

 

 




