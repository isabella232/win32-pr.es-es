---
title: Canal de seguridad Configuración
description: La configuración del canal de seguridad controla la forma en que se aplica y se comprueba la seguridad en un canal.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Servicios web Configuración canal de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467028"
---
# <a name="security-channel-settings"></a>Canal de seguridad Configuración

La configuración del canal de seguridad controla la forma en que se aplica y se comprueba la seguridad en un canal. Cada configuración de canal de seguridad se representa mediante una colección de pares propiedad-valor, con las claves de propiedad definidas por el id. de [**propiedad de WS \_ SECURITY de \_ \_ enumeración.**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) Cada propiedad de la colección tiene un valor predeterminado razonable. Debido a estos valores predeterminados, es posible definir y usar una descripción de seguridad sin especificar ninguna de las opciones del canal de seguridad.


[La configuración de enlace de](security-binding-settings.md) seguridad contiene colecciones similares de pares propiedad-valor cuyas claves se definen mediante la estructura [**\_ WS SECURITY BINDING \_ \_ PROPERTY.**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) La diferencia entre estos dos tipos de configuración es que la configuración del canal de seguridad está en el ámbito de una descripción de seguridad (es decir, contienen propiedades de seguridad para todo el canal), mientras que la configuración de enlace de seguridad está en el ámbito de uno de los enlaces de seguridad y puede haber muchos enlaces de seguridad. Por lo tanto, por ejemplo, una descripción de seguridad personalizada que contiene tres enlaces de seguridad tendrá una bolsa de configuración del canal de seguridad para todo el canal y tres bolsa de configuración de enlace de seguridad, una para cada enlace de seguridad.

Las enumeraciones siguientes se usan con la configuración del canal de seguridad:

-   [**NIVEL DE PROTECCIÓN DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [**IDENTIFICADOR DE PROPIEDAD \_ DEL TOKEN DE SEGURIDAD DE \_ \_ \_ WS \_ REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [**IDENTIFICADOR DEL \_ ALGORITMO \_ DE SEGURIDAD DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [**IDENTIFICADOR DE PROPIEDAD \_ DEL ALGORITMO DE SEGURIDAD \_ \_ DE \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [**DISEÑO DEL ENCABEZADO \_ DE \_ SEGURIDAD DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [**VERSIÓN DEL \_ ENCABEZADO DE \_ SEGURIDAD DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [**ID. \_ DE PROPIEDAD DE SEGURIDAD \_ DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**USO DE MARCA \_ DE TIEMPO DE \_ SEGURIDAD DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [**IDENTIFICADOR DE PROPIEDAD \_ DEL TOKEN DE SEGURIDAD \_ \_ DE \_ \_ WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

Las estructuras siguientes se usan con la configuración del canal de seguridad:

-   [**WS \_ REQUEST \_ SECURITY \_ TOKEN \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [**PROPIEDAD DEL \_ ALGORITMO \_ DE SEGURIDAD DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [**CONJUNTO DE ALGORITMOS \_ \_ DE SEGURIDAD DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [**WS \_ SECURITY \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [**WS \_ XML \_ SECURITY \_ TOKEN \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




