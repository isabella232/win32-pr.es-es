---
title: Configuración del canal de seguridad
description: La configuración del canal de seguridad controla la manera en que se aplica y se comprueba la seguridad en un canal.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Servicios Web de configuración del canal de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149740"
---
# <a name="security-channel-settings"></a>Configuración del canal de seguridad

La configuración del canal de seguridad controla la manera en que se aplica y se comprueba la seguridad en un canal. Cada configuración de canal de seguridad se representa mediante una colección de pares propiedad-valor, con las claves de propiedad definidas por el identificador de la [**\_ \_ propiedad \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)de la enumeración. Cada propiedad de la colección tiene un valor predeterminado razonable. Debido a estos valores predeterminados, es posible definir y usar una descripción de seguridad sin especificar ninguna configuración de canal de seguridad.


La [configuración de enlace de seguridad](security-binding-settings.md) contiene colecciones similares de pares de valor y propiedad cuyas claves están definidas por la estructura de la [**\_ \_ \_ propiedad de enlace de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) . La diferencia entre estos dos tipos de configuración es que la configuración del canal de seguridad se limita a una descripción de seguridad (es decir, que contiene propiedades de seguridad de todo el canal), mientras que la configuración de enlace de seguridad se limita a uno de los enlaces de seguridad y puede haber muchos enlaces de seguridad. Por lo tanto, por ejemplo, una descripción de seguridad personalizada que contiene tres enlaces de seguridad tendrá un contenedor de configuración del canal de seguridad para todo el canal y tres bolsas de configuración de enlace de seguridad, uno para cada enlace de seguridad.

Las enumeraciones siguientes se usan con la configuración del canal de seguridad:

-   [**\_nivel de protección de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [**identificador de la \_ propiedad de token de seguridad de solicitud WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [**\_identificador del \_ algoritmo de seguridad de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [**identificador de la propiedad del algoritmo WS \_ Security \_ \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [**\_diseño del \_ encabezado de seguridad de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [**versión del encabezado de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [**identificador de la propiedad de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**uso de la marca de tiempo de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [**identificador de la propiedad de token de seguridad de WS \_ XML \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

Las siguientes estructuras se usan con la configuración del canal de seguridad:

-   [**\_propiedad de \_ token de seguridad de solicitud WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [**\_propiedad del \_ algoritmo de seguridad de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [**\_conjunto de \_ algoritmos de WS Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [**\_propiedad WS Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [**\_propiedad de \_ token de seguridad \_ \_ de WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




