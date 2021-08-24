---
title: Federación
description: La federación permite la delegación de autoridad de autorización a otros miembros de un interprise.
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- Servicios web de federación para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a902eb9469ad75e8c3c5a283284a009af11bb59b42470c91c39b1f16f83c61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703665"
---
# <a name="federation"></a>Federación

La federación permite la delegación de autoridad de autorización a otros miembros de un interprise. Por ejemplo, considere el siguiente problema empresarial: la empresa de fabricación de piezas automáticas Contoso Ltd quiere permitir que los empleados autorizados de su cliente Fabrikam Inc accedan de forma segura al servicio web de pedidos de piezas de Contoso. Una solución de seguridad para este escenario es que Contoso configure un mecanismo de confianza con Fabrikam para delegar la decisión de autorización de acceso en Fabrikam. Este proceso podría funcionar de la siguiente manera:

-   Fabrikam, cuando se convierte en asociado de Contoso, configura un acuerdo de confianza con Contoso. El objetivo de este paso es acordar el tipo de token de seguridad y el contenido que representará la autorización de Fabrikam y será aceptable para Contoso. Por ejemplo, se puede decidir que un certificado X.509 de confianza con el nombre de sujeto "CN=Fabrikam Inc Supplier STS" debe firmar un token SAML para que el servicio web de Contoso acepte ese SAML. Además, se puede decidir que la notificación de seguridad en el token SAML emitido debe ser ' ' (para la autorización de búsqueda de partes) o ' ' (para la autorización de https://schemas.contoso.com/claims/lookup https://schemas.contoso.com/claims/order pedidos de partes).
-   Cuando un empleado de Fabrikam usa la aplicación de pedidos de elementos internos, primero se pone en contacto con un servicio de token de seguridad (STS) dentro de Fabrikam. Ese empleado se autentica mediante el mecanismo de seguridad interno de Fabrikam (por ejemplo Windows, un nombre de usuario o contraseña de dominio), se comprueba su autorización para pedir partes y se le emite un token SAML de corta duración que contiene las notificaciones adecuadas y firmado por el certificado X.509 decidido anteriormente. A continuación, la aplicación de pedidos de elementos se pone en contacto con el servicio Contoso que presenta el token SAML emitido para autenticarse y realizar la tarea de ordenación.

En este caso, el STS de Fabrikam actúa como "entidad emisora" y el servicio de elementos de Contoso actúa como "usuario de confianza". ![Diagrama que muestra un usuario emisor y un usuario de confianza en una federación.](images/stsmodel.png)

## <a name="federation-features"></a>Características de federación

Estas son las características de seguridad admitidas para las partes o roles implicados en un escenario de federación:

-   Lado cliente: para obtener el token de seguridad del STS, se puede usar la [**función WsRequestSecurityToken.**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) Como alternativa, se puede usar una biblioteca de proveedores de tokens de seguridad del lado cliente como CardSpace o LiveID y, a continuación, usar su salida para crear localmente un token de seguridad mediante [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). En cualquier caso, una vez que el cliente tiene el token de seguridad, puede crear un canal al servicio especificando [**WS \_ XML TOKEN MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) para presentar el token, junto con un enlace de seguridad de transporte como [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) para proteger el canal.
-   Lado servidor: en un escenario de federación con un servicio de token de seguridad que emite tokens SAML, el servidor puede usar [**WS \_ SAML MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding), junto con un enlace de seguridad de transporte como [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) para proteger el canal.
-   STS: tenga en cuenta que el STS es una aplicación de servicio web y puede especificar [](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) los requisitos de seguridad para aquellos que solicitan un token de seguridad mediante una estructura de descripción de seguridad en el momento de la creación del agente de escucha igual que cualquier otro servicio web seguro. A continuación, puede analizar las cargas de mensajes de solicitud entrantes para validar las solicitudes de token y enviar tokens emitidos de vuelta como cargas de mensajes de respuesta. Actualmente, no se proporcionan características para ayudar a estos pasos de análisis y emisión.

Tenga en cuenta que el lado cliente puede controlar el token de seguridad emitido genéricamente como un token de seguridad XML sin conocer el tipo de token ni realizar un procesamiento específico del tipo de token. Sin embargo, el servidor tiene que comprender el tipo de token de seguridad específico para entenderlo y procesarlo. Los pasos de solicitud y respuesta del token de seguridad usan las construcciones definidas en la especificación WS-Trust seguridad.

## <a name="more-complex-federation-scenarios"></a>Escenarios de federación más complejos

Un escenario de federación puede implicar varios STS que forman una cadena de federación. Considere el ejemplo siguiente:

-   El cliente se autentica en el STS de LiveID mediante un nombre de usuario o contraseña de LiveID y obtiene un token de seguridad T1.
-   El cliente se autentica en STS1 mediante T1 y obtiene un token de seguridad T2.
-   El cliente se autentica en STS2 mediante T2 y obtiene un token de seguridad T3.
-   El cliente se autentica en el servicio de destino S mediante T3.

Aquí, liveID STS, STS1, STS2 y S forman la cadena de federación. Los STS de una cadena de federación pueden realizar varios roles para el escenario general de la aplicación. Algunos ejemplos de estos roles funcionales de STS son el proveedor de identidades, el responsable de la toma de decisiones de autorización, el anonimizador y el administrador de recursos.

## <a name="sts-request-parameters-and-metadata-exchange"></a>Parámetros de solicitud y metadatos de STS Exchange

Para que el cliente realice una llamada correcta a [**WsRequestSecurityToken,**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) debe conocer los parámetros de [](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) esa llamada (como el tipo de token [](endpoint-address.md) y los tipos de notificación necesarios), los requisitos de descripción de seguridad del canal de solicitud al STS y la dirección del punto de conexión del STS. La aplicación cliente puede usar cualquiera de las técnicas siguientes para determinar esta información:

-   Codimente la información de la aplicación como parte de las decisiones en tiempo de diseño.
-   Lea esta información de un archivo de configuración de nivel de aplicación configurado por el implementador de aplicaciones local.
-   Detecte dinámicamente esta información en tiempo de ejecución mediante la característica [de](metadata-import.md) importación de metadatos con la estructura [**WS \_ ISSUED TOKEN MESSAGE SECURITY \_ BINDING \_ \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Para ilustrar el uso de MEX dinámico con la federación, considere el ejemplo de 3 STS anterior. En primer lugar, el cliente realizará un MEX dinámico con S para obtener información sobre T3 (es decir, qué preguntar a STS2), así como la dirección MEX dinámica de STS2 (es decir, dónde encontrar STS2). A continuación, usará esa información para realizar un MEX dinámico con STS2 para detectar información sobre T2 y STS1, y así sucesivamente.

Por lo tanto, los pasos de MEX dinámicos se llevan a cabo en el orden 4, 3, 2, 1 para compilar la cadena de federación y los pasos de solicitud y presentación de tokens se llevan a cabo en el orden 1, 2, 3, 4 para desenredar la cadena de federación.

> [!Note]  
> Windows 7 y Windows Server 2008 R2: WWSAPI solo admite [Ws-Trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) y [Ws-SecureConversation,](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) tal como se define en [Lightweight Seguridad de Servicios web Profile (LWSSP).](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e) Para más información sobre la implementación de Microsoft, consulte la sección [Sintaxis message](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) de LWSSP.

 

 

 