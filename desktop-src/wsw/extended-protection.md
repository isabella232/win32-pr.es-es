---
title: protección ampliada
description: La protección ampliada es un mecanismo para enlazar un canal seguro externo, como SSL, a protocolos de autenticación de canal interno, como Kerberos-APREQ y autenticación de encabezado HTTP.
ms.assetid: 35e48846-05e5-4db9-a3b5-098b62815b66
keywords:
- Protección ampliada Native-Web-Services
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e327d929b77108c1b675e6f42a311e4cad6dd9a056e5ac38b6d7e7f4558788c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927550"
---
# <a name="extended-protection"></a>protección ampliada

La protección ampliada es un mecanismo para enlazar un canal seguro externo, como SSL, a protocolos de autenticación de canal interno, como Kerberos-APREQ y autenticación de encabezado HTTP.

El concepto de protección ampliada se define en RFC2743.

La protección ampliada, cuando está disponible, se configura automáticamente en el cliente, pero puede requerir la configuración en el servidor para escenarios no predeterminados.

## <a name="supported-configurations"></a>Configuraciones admitidas

Se admite la protección ampliada cuando se usa [**WS \_ HTTP CHANNEL \_ \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) con enlaces de seguridad mediante protocolos de autenticación integrada de Windows, como [**WS HTTP HEADER \_ \_ \_ AUTH SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) y [**WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding). Se configura a través de las siguientes [**propiedades de seguridad:**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)

-   [**DIRECTIVA DE \_ PROTECCIÓN AMPLIADA DE LA PROPIEDAD DE \_ \_ \_ SEGURIDAD \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**ESCENARIO DE \_ PROTECCIÓN EXTENDIDA DE LA PROPIEDAD DE \_ \_ \_ SEGURIDAD \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**IDENTIDADES DEL \_ SERVICIO DE PROPIEDADES DE SEGURIDAD \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

Las siguientes configuraciones que implican la protección ampliada son posibles:

Cliente

-   [**WS \_ EL \_ ENLACE DE SEGURIDAD DE \_ \_ TRANSPORTE**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) SSL se usa con [**WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) o [**WS HTTP HEADER \_ \_ \_ AUTH SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). En esta configuración, el enlace de autenticación se enlaza a la conexión SSL a través de un token de protección extendida que se extrae automáticamente de la conexión SSL.
-   No se usa SSL y [**se establece WS \_ HTTP HEADER \_ \_ AUTH SECURITY \_ \_ BINDING.**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) El enlace de autenticación se enlaza a través del nombre principal del servidor (SPN), que se determina automáticamente a partir de la dirección del punto de conexión [**de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address).

Servidor

-   [**WS \_ EL \_ ENLACE DE SEGURIDAD DE \_ \_ TRANSPORTE**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) SSL se usa con [**WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) o [**WS HTTP HEADER \_ \_ \_ AUTH SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). En esta configuración, el enlace de autenticación se enlaza a la conexión SSL a través de un token de protección extendida que se extrae de la conexión SSL y se valida automáticamente.
-   No se usa SSL y [**se establece WS \_ HTTP HEADER \_ \_ AUTH SECURITY \_ \_ BINDING.**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) El enlace de autenticación se enlaza a través del nombre principal del servidor (SPN), que se debe proporcionar a través de [**WS \_ SECURITY PROPERTY \_ SERVICE \_ \_ IDENTITIES**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id). Cuando se recibe un mensaje, el SPN se extrae y valida para una coincidencia exacta con los nombres de servicio proporcionados. No proporcionar SPN equivale a establecer [**WS \_ EXTENDED PROTECTION POLICY \_ \_ \_ NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy).
-   No se usa SSL, [**se especifica WS \_ EXTENDED PROTECTION SCENARIO BOUND \_ \_ \_ \_ SERVER**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) y [**se usa WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING.**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) En esta configuración, [**WS \_ SECURITY PROPERTY \_ SERVICE \_ \_ IDENTITIES**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) no debe establecerse. No se realiza ninguna comprobación de SPN más allá de lo que se hace como parte del protocolo Kerberos.
-   [**WS \_ Se \_ especifica EXTENDED PROTECTION SCENARIO TERMINATED \_ \_ \_ SSL**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) y se usa [**WS KERBEROS \_ \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) o [**WS HTTP HEADER \_ \_ \_ AUTH SECURITY \_ \_ BINDING.**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) [**WS \_ Security \_ PROPERTY \_ SERVICE \_ IDENTITIES**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) debe establecerse.

## <a name="supported-platforms"></a>Plataformas compatibles

La protección ampliada se admite en plataformas compatibles con él en el sistema operativo. Windows 7 y Windows Server 2008 R2 proporcionan compatibilidad integrada. Otras plataformas pueden requerir una actualización.

Si el sistema operativo del servidor no proporciona este tipo de compatibilidad, se omite cualquier información de protección extendida enviada por el cliente. Como resultado, los clientes que usan la protección ampliada pueden comunicarse con este tipo de servidor, pero se pierde la ventaja de seguridad. En el cliente, [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) combinado con [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) solo admite la protección ampliada en Vista y versiones posteriores.

NOTA: La protección ampliada que no está disponible no impide que se utilice una configuración determinada.

## <a name="interoperability"></a>Interoperabilidad

Un servidor configurado de forma predeterminada puede comunicarse con los clientes SOAP independientemente de si usan o no la protección ampliada. Una excepción que es Windows XP y Windows Server 2003 WWSAPI que se han actualizado para admitir la protección ampliada y usan [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) y [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Para admitir dichos [**clientes, WS \_ EXTENDED PROTECTION POLICY \_ \_ \_ NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy) debe especificarse por el servidor. Los servidores **configurados con WS \_ EXTENDED PROTECTION POLICY \_ \_ \_ SIEMPRE** rechazarán la comunicación de los clientes que no usan la protección ampliada. En el cliente, **WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING** combinado con **WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING** dará lugar a que el mensaje se envíe mediante la codificación de transferencia fragmentada HTTP en Vista y versiones posteriores. Esto puede provocar problemas de interoperabilidad con servidores que no admiten la transferencia fragmentada.

Las siguientes enumeraciones o constantes forman parte de la protección ampliada:

-   [**DIRECTIVA DE \_ PROTECCIÓN \_ AMPLIADA DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy)
-   [**ESCENARIO DE PROTECCIÓN \_ \_ AMPLIADA DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario)

Las siguientes escotes forman parte de la protección ampliada:

-   [**IDENTIDADES DE \_ SEGURIDAD \_ DEL SERVICIO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_security_identities)

 

 




