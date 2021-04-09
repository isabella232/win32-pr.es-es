---
title: Enlaces de seguridad
description: Un enlace de seguridad es la especificación de un token de seguridad e indica al tiempo de ejecución cómo obtener y usar un token de seguridad para la seguridad del canal.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Servicios Web de enlaces de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149734"
---
# <a name="security-bindings"></a>Enlaces de seguridad

Un enlace de seguridad es la especificación de un token de seguridad e indica al tiempo de ejecución cómo obtener y usar un token de seguridad para la seguridad del canal. El token de seguridad contiene información que garantiza el derecho a tener acceso a los recursos. También puede tener una clave criptográfica asociada para realizar firmas y cifrado.


Cada enlace de seguridad contiene su propia colección de [Opciones de enlace de seguridad](security-binding-settings.md) opcionales cuyo ámbito es el token de seguridad que define. También contiene [credenciales de seguridad](security-credentials.md), que representan la evidencia de seguridad (como el nombre de usuario y contraseñas o los certificados) necesarios para crear tokens de seguridad.

Las siguientes devoluciones de llamada forman parte del enlace de seguridad:

-   [**\_devolución de \_ llamada de SAML Validate de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

Las enumeraciones siguientes forman parte del enlace de seguridad:

-   [**\_uso de \_ seguridad de mensajes de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**\_tipo de \_ autenticador \_ SAML de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**tipo de enlace de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**\_tipo de \_ identificador de clave \_ \_ de WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

Las siguientes funciones forman parte del enlace de seguridad:

-   [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**WsFreeSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

Las siguientes estructuras forman parte del enlace de seguridad:

-   [**\_identificador de \_ \_ clave de seguridad asimétrica \_ \_ de WS CAPI**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**\_ \_ \_ autenticador SAML firmado de certificado WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**\_enlace de \_ \_ seguridad de autenticación de encabezado HTTP \_ de \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**\_enlace de \_ \_ seguridad de mensajes WS Kerberos APREQ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**\_enlace de \_ \_ seguridad de transporte SSPI \_ \_ de WS NAMEDPIPE**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**\_identificador de \_ \_ clave de seguridad asimétrica \_ \_ de WS NCRYPT**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**\_identificador de \_ \_ clave de seguridad simétrica sin \_ procesar \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**\_autenticador de SAML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**\_enlace de \_ seguridad de mensajes SAML \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**\_enlace de seguridad de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**\_enlace de \_ seguridad de mensaje de contexto \_ \_ de WS Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**identificador de clave de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**\_enlace de \_ seguridad de transporte WS SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**\_enlace de \_ \_ seguridad de transporte SSPI \_ \_ de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**\_enlace de \_ seguridad de mensaje \_ \_ de WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**\_enlace de \_ seguridad de mensaje de token \_ \_ de WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




