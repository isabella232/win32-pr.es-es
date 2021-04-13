---
title: Federación
description: La Federación permite la delegación de autoridad de autorización a otros miembros de una instancia de.
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- Servicios Web de Federación para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a02744c9c0a5358da35f4c31c20633c420fee9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104555169"
---
# <a name="federation"></a>Federación

La Federación permite la delegación de autoridad de autorización a otros miembros de una instancia de. Por ejemplo, tenga en cuenta el siguiente problema empresarial: la empresa auto Manufacturing Company contoso Ltd desea permitir que los empleados autorizados de su cliente Fabrikam Inc accedan de forma segura al servicio Web de pedidos de piezas de contoso. Una solución de seguridad para este escenario es que contoso establezca un mecanismo de confianza con Fabrikam para delegar la decisión de autorización de acceso a fabrikam. Este proceso podría funcionar de la siguiente manera:

-   Fabrikam, cuando se convierte en socio de Contoso, configura un acuerdo de confianza con contoso. El objetivo de este paso es acordar el tipo de token de seguridad y el contenido que representará la autorización de Fabrikam, y será aceptable para contoso. Por ejemplo, se puede decidir que un certificado X. 509 de confianza con el nombre de sujeto "CN = Fabrikam Inc Supplier STS" debe firmar un token SAML para que SAML lo acepte el servicio Web de contoso. Además, se puede decidir que la demanda de seguridad en el token SAML emitido debe ser ' https://schemas.contoso.com/claims/lookup ' (para la autorización de búsqueda de piezas) o ' https://schemas.contoso.com/claims/order ' (para la autorización de ordenación de partes).
-   Cuando un empleado de Fabrikam usa la aplicación de pedidos de piezas internas, primero se pone en contacto con un servicio de token de seguridad (STS) dentro de fabrikam. Ese empleado se autentica mediante el mecanismo de seguridad interno de Fabrikam (por ejemplo, nombre de usuario y contraseña de dominio de Windows), se comprueba la autorización de los elementos de pedido y se emite un token SAML de corta duración que contiene las notificaciones adecuadas y firmado por el certificado X. 509 que se decidió anteriormente. A continuación, la aplicación de pedidos de piezas se pone en contacto con el servicio de Contoso que presenta el token SAML emitido para autenticarse y realizar la tarea de ordenación.

En este caso, el STS de Fabrikam actúa como la "entidad emisora" y el servicio de piezas de Contoso actúa como el "usuario de confianza". ![Diagrama que muestra una entidad emisora y un usuario de confianza en una Federación.](images/stsmodel.png)

## <a name="federation-features"></a>Características de Federación

A continuación se indican las características de seguridad admitidas para las entidades o los roles implicados en un escenario de Federación:

-   Lado cliente: para obtener el token de seguridad del STS, puede usar la función [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) . Como alternativa, puede usar una biblioteca del proveedor de tokens de seguridad del lado cliente como CardSpace o LiveID y, a continuación, usar la salida para crear localmente un token de seguridad mediante [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). En cualquier caso, una vez que el cliente tenga el token de seguridad, puede crear un canal para el servicio especificando el [**enlace de seguridad de mensaje de token de WS \_ XML \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) para presentar el token, junto con un enlace de seguridad de transporte como el enlace de [**\_ seguridad de \_ transporte \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) para proteger el canal.
-   Lado servidor: en un escenario de Federación con un servicio de token de seguridad que emite tokens SAML, el servidor puede usar el [**\_ enlace de seguridad de \_ mensajes \_ \_ WS SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding), junto con un enlace de seguridad de transporte como el [**enlace de \_ seguridad de \_ transporte \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) para proteger el canal.
-   STS-Side: tenga en cuenta que el STS es una aplicación de servicio Web y puede especificar los requisitos de seguridad para los que solicitan un token de seguridad de él mediante una estructura de [**Descripción de seguridad**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) en el momento de creación del agente de escucha de la misma forma que cualquier otro servicio Web seguro. A continuación, puede analizar las cargas de mensajes de solicitud entrantes para validar las solicitudes de token y devolver los tokens emitidos como cargas de mensajes de respuesta. Actualmente, no se proporcionan características que ayuden a analizar y emitir pasos.

Tenga en cuenta que el lado cliente puede controlar el token de seguridad emitido de forma genérica como un token de seguridad XML sin conocer el tipo de token o realizar el procesamiento específico del tipo de token. Sin embargo, el servidor tiene que entender el tipo de token de seguridad específico para poder comprenderlo y procesarlo. Los pasos de solicitud y respuesta del token de seguridad usan las construcciones definidas en la especificación WS-Trust.

## <a name="more-complex-federation-scenarios"></a>Escenarios de Federación más complejos

Un escenario de Federación puede implicar varios STS que forman una cadena de Federación. Considere el ejemplo siguiente:

-   El cliente se autentica en el STS de LiveID mediante un nombre de usuario y contraseña de LiveID y obtiene un token de seguridad T1.
-   El cliente se autentica en STS1 con T1 y obtiene un token de seguridad T2.
-   El cliente se autentica en STS2 con T2 y obtiene un token de seguridad T3.
-   El cliente se autentica en el servicio de destino con T3.

Aquí, el STS de LiveID, STS1, STS2 y S forman la cadena de Federación. El STS de una cadena de Federación puede realizar varios roles para el escenario de aplicación general. Entre los ejemplos de estos roles funcionales de STS se incluyen proveedor de identidades, responsable de decisiones de autorización, Anonymizer y Resource Manager.

## <a name="sts-request-parameters-and-metadata-exchange"></a>Parámetros de solicitud y intercambio de metadatos de STS

Para que el cliente realice una llamada [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) correcta, debe conocer los parámetros de esa llamada (como el tipo de token y los tipos de notificaciones necesarios), los requisitos de [**Descripción de seguridad**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) del canal de solicitud al STS y la dirección del [punto de conexión](endpoint-address.md) del STS. La aplicación cliente puede utilizar cualquiera de las técnicas siguientes para determinar esta información:

-   Codifique la información de la aplicación como parte de las decisiones de tiempo de diseño.
-   Lea esta información de un archivo de configuración de nivel de aplicación configurado por el implementador de la aplicación local.
-   Detecte dinámicamente esta información en tiempo de ejecución mediante la característica de [importación de metadatos](metadata-import.md) con la estructura de [**restricción de enlace de \_ \_ seguridad de mensaje de token \_ \_ \_ \_ emitido de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .

Para ilustrar el uso de MEX dinámico con la Federación, considere el ejemplo 3 STS anterior. El cliente realizará primero un MEX dinámico con S para obtener información sobre T3 (es decir, qué se debe preguntar desde STS2), así como la dirección MEX dinámica de STS2 (es decir, dónde encontrar STS2). A continuación, usará esa información para realizar una MEX dinámica con STS2 para detectar información sobre T2 y STS1, etc.

Por lo tanto, los pasos de MEX dinámico tienen lugar en el orden 4, 3, 2, 1 para crear la cadena de Federación y los pasos de solicitud y presentación de tokens tienen lugar en el orden 1, 2, 3, 4 para desenredar la cadena de Federación.

> [!Note]  
> Windows 7 y Windows Server 2008 R2: WWSAPI solo admite [WS-Trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) y [WS-SecureConversation](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) , tal y como se define en [Lightweight seguridad de servicios web Profile (LWSSP)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Para obtener más información sobre la implementación de Microsoft, consulte la sección sobre la [Sintaxis del mensaje](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) de LWSSP.

 

 

 