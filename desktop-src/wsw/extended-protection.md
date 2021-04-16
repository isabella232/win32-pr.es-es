---
title: protección ampliada
description: La protección ampliada es un mecanismo para enlazar un canal seguro externo, como SSL, a protocolos de autenticación de canal interno como Kerberos-APREQ y la autenticación de encabezados HTTP.
ms.assetid: 35e48846-05e5-4db9-a3b5-098b62815b66
keywords:
- Protección ampliada Native-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895bdfecf994f6673c2ed7e7367bc3a7b5bd70c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685572"
---
# <a name="extended-protection"></a>protección ampliada

La protección ampliada es un mecanismo para enlazar un canal seguro externo, como SSL, a protocolos de autenticación de canal interno como Kerberos-APREQ y la autenticación de encabezados HTTP.

El concepto de protección ampliada se define en RFC2743.

La protección ampliada, si está disponible, se configura automáticamente en el cliente, pero puede que sea necesario configurar en el servidor para escenarios no predeterminados.

## <a name="supported-configurations"></a>Configuraciones admitidas

La protección ampliada se admite cuando se usa el [**\_ enlace de \_ canal \_ WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) con enlaces de seguridad mediante protocolos de autenticación integrada de Windows, como el [**\_ \_ \_ \_ \_ enlace de seguridad de encabezados HTTP WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) y el enlace de seguridad de [**\_ mensajes WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding). Se configura a través de las siguientes [**propiedades de seguridad**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property):

-   [**\_Directiva de \_ \_ protección extendida de propiedades \_ \_ de WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_escenario de \_ \_ protección ampliada de propiedades \_ \_ de WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_ \_ \_ identidades de servicio de propiedades \_ de WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

Se pueden realizar las siguientes configuraciones que impliquen protección ampliada:

Remoto

-   [**WS \_ El \_ \_ \_ enlace de seguridad de transporte SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) se utiliza con el enlace de seguridad de [**\_ mensaje WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) o el enlace de seguridad de la [**\_ \_ autenticación del encabezado \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). En esta configuración, el enlace de autenticación se enlaza a la conexión SSL a través de un token de protección ampliada que se extrae automáticamente de la conexión SSL.
-   No se usa SSL y se establece el [**enlace de seguridad de \_ \_ autenticación de encabezado \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) . El enlace de autenticación se enlaza a través del nombre de entidad de seguridad de servidor (SPN), que es autonatically determinado a partir de la [**\_ \_ dirección del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address).

Servidor

-   [**WS \_ El \_ \_ \_ enlace de seguridad de transporte SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) se utiliza con el enlace de seguridad de [**\_ mensaje WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) o el enlace de seguridad de la [**\_ \_ autenticación del encabezado \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). En esta configuración, el enlace de autenticación se enlaza a la conexión SSL a través de un token de protección ampliada que se extrae de la conexión SSL y se valida automáticamente.
-   No se usa SSL y se establece el [**enlace de seguridad de \_ \_ autenticación de encabezado \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) . El enlace de autenticación se enlaza a través del nombre de entidad de seguridad de servidor (SPN), que debe proporcionarse a través de las [**\_ \_ \_ \_ identidades de servicio de propiedades de WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id). Cuando se recibe un mensaje, se extrae y valida el SPN para obtener una coincidencia exacta con los nombres de servicio proporcionados. No proporcionar SPN es el equivalente a establecer [**\_ nunca la \_ \_ Directiva de \_ protección ampliada de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy).
-   No se usa SSL, se especifica el [**\_ \_ \_ \_ \_ servidor enlazado con el escenario de protección ampliada de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) y se usa el [**enlace de seguridad de \_ mensajes WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) . En esta configuración, no se deben establecer las [**\_ \_ \_ \_ identidades de servicio de las propiedades de WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) . No se realiza ninguna comprobación de SPN más allá de lo que se hace como parte del protocolo Kerberos.
-   [**WS \_ Escenario de protección AMPLIAda se ha especificado \_ \_ \_ \_ SSL finalizado**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) y se usa el enlace de seguridad de [**\_ mensaje WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) o de [**\_ \_ autenticación de encabezado \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) . [**WS \_ Se deben establecer las \_ \_ \_ identidades de servicio**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) de la propiedad de seguridad.

## <a name="supported-platforms"></a>Plataformas compatibles

La protección ampliada es compatible con las plataformas que admiten en el sistema operativo. Windows 7 y Windows Server 2008 R2 proporcionan compatibilidad integrada. Es posible que otras plataformas requieran una actualización.

Si el sistema operativo del servidor no proporciona dicha compatibilidad, se omite cualquier información de protección ampliada enviada por el cliente. Como resultado, los clientes que usan la protección ampliada pueden comunicarse con este servidor, pero se pierde la ventaja de seguridad. En el cliente, [**el \_ \_ enlace de \_ \_ seguridad de \_ mensajes WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) combinado con el [**\_ \_ \_ \_ enlace de seguridad de transporte SSL de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) solo admite la protección ampliada en vista y versiones posteriores.

Nota: la protección ampliada no está disponible no impide que se use ninguna configuración determinada.

## <a name="interoperability"></a>Interoperabilidad

Un servidor configurado de forma predeterminada puede comunicarse con los clientes SOAP independientemente de si usan la protección ampliada o no. La única excepción son los clientes de Windows XP y Windows Server 2003 WWSAPI que se han actualizado para admitir la protección ampliada y utilizan el enlace de seguridad de [**\_ mensajes WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) y el enlace de [**seguridad de \_ \_ transporte \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Para admitir estos clientes, el servidor no debe especificar [**\_ nunca la \_ \_ directiva \_ de protección ampliada de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy) . Los servidores configurados con la **\_ Directiva de protección ampliada de WS \_ \_ \_ siempre** rechazarán la comunicación de los clientes que no usen la protección ampliada. En el cliente, **el \_ \_ enlace de \_ \_ seguridad de \_ mensajes WS Kerberos APREQ** combinado con el **\_ \_ \_ \_ enlace de seguridad de transporte SSL de WS** dará como resultado que el mensaje se envíe mediante la codificación de transferencia fragmentada http en vista y versiones posteriores. Esto puede producir problemas de interoperabilidad con servidores que no admiten la transferencia fragmentada.

Las enumeraciones o constantes siguientes forman parte de la protección ampliada:

-   [**\_Directiva de \_ protección ampliada de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy)
-   [**\_escenario de \_ protección ampliada de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario)

Los siguientes estructuras forman parte de la protección ampliada:

-   [**\_ \_ identidades de seguridad de servicio de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_security_identities)

 

 




