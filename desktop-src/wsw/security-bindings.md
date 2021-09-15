---
title: Enlaces de seguridad
description: Un enlace de seguridad es la especificación de un token de seguridad e indica al tiempo de ejecución cómo obtener y usar un token de seguridad para la seguridad del canal.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Servicios web de enlaces de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467030"
---
# <a name="security-bindings"></a>Enlaces de seguridad

Un enlace de seguridad es la especificación de un token de seguridad e indica al tiempo de ejecución cómo obtener y usar un token de seguridad para la seguridad del canal. El token de seguridad contiene información que se utiliza para el derecho de acceso a los recursos. También puede tener una clave criptográfica asociada para realizar firmas y cifrado.


Cada enlace de seguridad contiene su propia colección de opciones de enlace [de seguridad opcionales](security-binding-settings.md) que tienen como ámbito el token de seguridad que define. También contiene credenciales [de seguridad](security-credentials.md), que representan la evidencia de seguridad (como el nombre de usuario y las contraseñas, o los certificados) necesarios para crear tokens de seguridad.

Las devoluciones de llamada siguientes forman parte del enlace de seguridad:

-   [**WS \_ VALIDATE \_ SAML \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

Las enumeraciones siguientes forman parte del enlace de seguridad:

-   [**USO DE SEGURIDAD \_ DE \_ MENSAJES WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**WS \_ SAML \_ AUTHENTICATOR \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**TIPO DE \_ ENLACE DE \_ SEGURIDAD DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**TIPO DE IDENTIFICADOR \_ DE CLAVE DE SEGURIDAD \_ \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

Las siguientes funciones forman parte del enlace de seguridad:

-   [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**WsFreeSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

Las estructuras siguientes forman parte del enlace de seguridad:

-   [**IDENTIFICADOR DE CLAVE \_ DE SEGURIDAD \_ \_ ASIMÉTRICA DE \_ \_ WS CAPI**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**AUTENTICADOR \_ \_ SAML FIRMADO POR EL \_ CERTIFICADO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**ENLACE DE \_ SEGURIDAD DE AUTENTICACIÓN DE ENCABEZADO HTTP \_ \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**ENLACE DE SEGURIDAD DE TRANSPORTE DE WS \_ NAMEDPIPE \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**IDENTIFICADOR DE CLAVE \_ DE \_ SEGURIDAD \_ ASIMÉTRICA DE \_ \_ WS NCRYPT**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**IDENTIFICADOR DE CLAVE \_ DE \_ SEGURIDAD \_ SIMÉTRICA SIN \_ \_ PROCESAR DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**WS \_ SAML \_ AUTHENTICATOR**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**WS \_ SAML \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**ENLACE DE SEGURIDAD DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**ENLACE DE \_ SEGURIDAD DE MENSAJES DE CONTEXTO DE \_ \_ \_ SEGURIDAD DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**IDENTIFICADOR DE CLAVE \_ \_ DE SEGURIDAD DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**ENLACE DE \_ SEGURIDAD DE TRANSPORTE SSL \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**ENLACE DE \_ SEGURIDAD DE TRANSPORTE DE WS TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**ENLACE DE SEGURIDAD \_ DE MENSAJES DE NOMBRE DE \_ \_ USUARIO DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**ENLACE DE \_ SEGURIDAD DE MENSAJES DE TOKEN XML \_ \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




