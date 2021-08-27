---
title: Información general sobre seguridad
description: El marco de seguridad de Windows Web Services API (WWSAPI) proporciona integridad de los mensajes, confidencialidad, detección de reproducción y autenticación del servidor mediante la seguridad de transporte.
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- Información general sobre seguridad Web Services for Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6928afd51ded7104e909994f8b625b931da6a157e859c890066c73074ae7d16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089445"
---
# <a name="security-overview"></a>Información general sobre seguridad

El marco de seguridad de Windows Web Services API (WWSAPI) proporciona:

-   Integridad de los mensajes, confidencialidad, detección de reproducción y autenticación del servidor mediante la seguridad de transporte.
-   Autenticación de cliente, como validación de tokens de seguridad, comprobaciones de revocación y confianza de certificados, etc. mediante seguridad de mensajes SOAP o seguridad de transporte.

## <a name="the-security-programming-model"></a>El modelo de programación de seguridad

La seguridad está asociada a los [canales de comunicación](channel-layer-overview.md). La protección de un canal consta de los pasos siguientes.

-   Cree e inicialice uno o varios [**enlaces de seguridad adecuados**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) para los requisitos de seguridad de la aplicación.
-   Cree una [**descripción de seguridad**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que contenga esos enlaces de seguridad.
-   Cree un proxy [**de**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) [**servicio o**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) canal (en el lado cliente) o cree un cliente de escucha o [**un host**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) de servicio (en el lado servidor) pasando esa descripción de seguridad. [](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   Realice los pasos normales de programación de canales de Open, Accept, Send, Receive, Close, etc.

El tiempo de ejecución protege automáticamente los mensajes enviados y recibidos en el canal según la descripción de seguridad proporcionada. Opcionalmente, estos pasos se pueden ajustar especificando [](security-channel-settings.md) una o varias opciones de [](security-binding-settings.md) seguridad de todo el canal en la descripción de seguridad o en la configuración de seguridad de todo el enlace en un enlace de seguridad.

La aplicación debe realizar cualquier autorización necesaria de identidades de remitente mediante los resultados [de procesamiento de seguridad](security-processing-results.md) asociados a cada mensaje recibido. Los pasos de autorización no se especifican en la descripción de seguridad ni el tiempo de ejecución realiza automáticamente.

Los errores en la descripción de seguridad, como enlaces no admitidos, propiedades o campos no aplicables, falta de propiedades o campos necesarios o valores de propiedad o campo no válidos, provocarán un error en la creación del canal o del agente de escucha.

## <a name="selecting-security-bindings"></a>Selección de enlaces de seguridad

Al diseñar la seguridad de una aplicación, la decisión principal es la selección de los enlaces de seguridad que se incluirán en la descripción de seguridad. Estas son algunas directrices para elegir enlaces de seguridad adecuados para el escenario de seguridad de una aplicación. Una heurística útil es comprender primero qué tipos de credenciales de seguridad (por ejemplo, certificados [**X.509**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential), nombre de usuario o contraseñas de dominio de Windows, nombre de usuario y contraseñas definidos por la [**aplicación)**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)estarán disponibles para la aplicación y, [**después,**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)elegir un enlace de seguridad que pueda usar ese tipo de credencial.

-   La seguridad de transporte, donde se aplica la seguridad en el nivel de flujo de bytes de transporte (por debajo de los límites del mensaje SOAP), es la primera opción que se debe tener en cuenta.
    -   Para escenarios de Internet y para aquellos escenarios de intranet en los que se puede implementar un certificado X.509 en el servidor, la aplicación puede usar [**WS \_ SSL TRANSPORT SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). En el ejemplo siguiente se muestra esta opción. Cliente: [HttpClientWithSslExample](httpclientwithsslexample.md) Server: [HttpServerWithSslExample](httpserverwithsslexample.md).

        Si se desea la autenticación de cliente a través de la autenticación de encabezado HTTP, se puede agregar un ENLACE DE SEGURIDAD DE [**\_ \_ \_ AUTENTICACIÓN \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) DE ENCABEZADO HTTP de WS para proporcionar esa funcionalidad.

    -   En los escenarios de intranet Windows protocolos de autenticación integrada como Kerberos, NTLM y SPNEGO son adecuados, la aplicación puede usar [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding). En el ejemplo siguiente se muestra esta opción: [Client: RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md) Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

        Cliente sobre canalizaciones con nombre: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        Servidor sobre canalizaciones con nombre: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   En escenarios de máquina local en los que Windows protocolos de autenticación integrada como Kerberos, NTLM y SPNEGO son adecuados, la aplicación puede usar [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) o [**WS \_ NAMEDPIPE \_ SSPI TRANSPORT SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding). El enlace de canal [**\_ WS \_ \_ NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) es preferible en estos escenarios porque garantiza que el tráfico no salga de la máquina (esta es la propiedad de **WS \_ NAMEDPIPE \_ CHANNEL \_ BINDING**).

-   La seguridad en modo mixto, donde la seguridad de transporte protege la conexión y un encabezado WS-Security en el mensaje SOAP proporciona autenticación de cliente, es la siguiente opción que se debe tener en cuenta. Los enlaces siguientes se usan junto con uno de los enlaces de seguridad de transporte descritos en la sección anterior.
    -   Cuando el cliente se autentica mediante un par de nombre de usuario y contraseña del nivel de aplicación, la aplicación puede usar un enlace [**WS \_ USERNAME MESSAGE SECURITY \_ \_ \_ para**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) proporcionar los datos de autenticación. En los ejemplos siguientes se muestra el uso de este enlace junto con un ENLACE [**DE SEGURIDAD DE TRANSPORTE SSL \_ \_ \_ de \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding):
        -   Cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)
        -   Servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)
    -   Cuando el cliente se autentica mediante un vale kerberos, la aplicación puede usar un ENLACE DE SEGURIDAD DE MENSAJES [**\_ \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) de WS KERBEROS para proporcionar los datos de autenticación.
    -   Cuando se usa [un contexto de seguridad](security-context.md), el cliente establece primero un contexto de seguridad con el servidor y, a continuación, usa ese contexto para autenticar los mensajes. Para habilitar esta funcionalidad, la descripción de seguridad debe contener un [**WS \_ SECURITY CONTEXT MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). Una vez establecidos, los contextos de seguridad se pueden transmitir mediante tokens ligeros, lo que evita tener que enviar las credenciales de cliente potencialmente grandes y costosas computacionalmente con cada mensaje.
    -   En un [escenario de](federation.md) seguridad federado, el cliente obtiene primero un token de seguridad emitido por un servicio de token de seguridad (STS) y, a continuación, presenta el token emitido a un servicio. Lado cliente: para obtener el token de seguridad del STS, la aplicación puede usar [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken). Como alternativa, la aplicación puede usar una biblioteca de proveedores de tokens de seguridad del lado cliente como CardSpace o LiveID y, a continuación, usar su salida para crear localmente un token de seguridad mediante [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). En cualquier caso, una vez que el token de seguridad está disponible para el cliente, se puede presentar al servicio mediante una descripción de seguridad que contiene un ENLACE DE SEGURIDAD DE MENSAJES DE TOKEN XML de [**WS \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding). Lado servidor: si el token de seguridad emitido por el STS es un token SAML, el servidor puede usar una descripción de seguridad con [**WS \_ SAML MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding).
        > [!Note]  
        > Windows 7 y Windows Server 2008 R2: WWSAPI solo admite [Ws-Trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) y [Ws-SecureConversation,](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) tal como se define en [Lightweight Seguridad de Servicios web Profile (LWSSP).](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e) Para más información sobre la implementación de Microsoft, consulte la [sección Sintaxis MESSAGE](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) de LWSSP.

         
-   La última opción a tener en cuenta es usar enlaces de autenticación sin usar un enlace de protección como [**WS \_ SSL TRANSPORT SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Esto dará lugar a que las credenciales se transmitan en texto sin formato y puede tener implicaciones de seguridad. El uso de esta opción debe evaluarse cuidadosamente para asegurarse de que no haya ninguna vulnerabilidad como resultado. Un ejemplo de uso potencial es intercambiar mensajes entre servidores back-end a través de una red privada segura. Las siguientes configuraciones admiten esta opción.

    -   [**WS \_ HTTP \_ HEADER \_ AUTH SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) admite esta opción en todas las configuraciones.
    -   [**WS \_ USERNAME \_ MESSAGE SECURITY BINDING \_ \_ admite**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) esta opción en el servidor cuando se usa HTTP como transporte.
    -   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) admite esta opción en el servidor cuando se usa HTTP como transporte.
    -   [**WS \_ SECURITY \_ CONTEXT MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) admite esta opción en el servidor cuando se usa HTTP como transporte.
    -   [**WS \_ SAML \_ MESSAGE SECURITY BINDING \_ \_ admite**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) esta opción en el servidor cuando se usa HTTP como transporte.

    La habilitación de esta opción requiere establecer explícitamente [**WS \_ PROTECTION \_ LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) en un valor distinto de **WS \_ PROTECTION LEVEL SIGN \_ AND \_ \_ \_ ENCRYPT**.

## <a name="channels-and-security"></a>Canales y seguridad

Como se indicó anteriormente, la seguridad está en el ámbito de los canales. Además, las operaciones de canal se asignan a los pasos de seguridad de forma coherente en todos los enlaces de seguridad.

-   Creación del canal: el conjunto de enlaces de seguridad especificado en la descripción de seguridad se valida y permanece fijo para el canal a partir de entonces. También se determina la forma de la pila de canales, incluidos los canales secundarios que se usarán para las WS-Trust basadas en el canal.
-   Canal abierto: se cargan las credenciales que se proporcionan como parte de los enlaces de seguridad y se establecen sesiones de seguridad. En general, un canal abierto contiene el estado de seguridad "en directo". Al abrir un canal de cliente también se especifica la dirección del punto de conexión del servidor en la que el tiempo de ejecución realizará la autenticación del servidor.
-   Entre el canal abierto y el cierre: los mensajes se pueden enviar y recibir de forma segura durante esta fase.
-   Envío de mensajes: los tokens de contexto de seguridad se obtienen o renuevan según sea necesario y la seguridad se aplica a cada mensaje transmitido según la descripción de seguridad. Los errores que se producen al aplicar la seguridad se devuelven a la aplicación como errores de envío.
-   Recepción de mensajes: la seguridad se comprueba en cada mensaje recibido según la descripción de seguridad. Los errores de comprobación de seguridad de mensajes se devuelven a la aplicación como errores de recepción. Estos errores por mensaje no afectan al estado del canal ni a las siguientes solicitudes. La aplicación puede descartar una recepción con error y reiniciar una recepción para otro mensaje.
-   Anulación del canal: el canal se puede anular en cualquier momento para detener todas las E/S del canal. Al anularse, el canal pasará a un estado de error y no permitirá más envíos ni recibir. Sin embargo, el canal todavía puede conservar algún estado de seguridad "en directo", por lo que será necesario un cierre posterior del canal para eliminar todo el estado de forma limpia.
-   Cierre del canal: se elimina el estado de seguridad creado al abrirse y se deshace la sesión. Se cancelan los tokens de contexto de seguridad. La pila del canal permanece, pero no contiene ningún estado de seguridad "en directo" ni credenciales cargadas.
-   Canal gratuito: se libera la pila de canales creada en la creación, junto con todos los recursos de seguridad.

## <a name="security-apis"></a>API de seguridad

La documentación de api de seguridad se agrupa en los temas siguientes.

-   [Descripción de seguridad](security-description.md)
    -   [Canal de seguridad Configuración](security-channel-settings.md)
    -   [Enlaces de seguridad](security-bindings.md)
        -   [Credenciales de seguridad](security-credentials.md)
        -   [Configuración de enlace de seguridad](security-binding-settings.md)
-   [Federación](federation.md)
-   [Contexto de seguridad](security-context.md)
-   [Identidad de extremo](endpoint-identity.md)
-   [Resultados del procesamiento de seguridad](security-processing-results.md)

## <a name="security"></a>Seguridad

Al usar la aplicación WWSAPI API para seguridad, las aplicaciones se enfrentan a varios riesgos de seguridad:

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>Error de configuración accidental
</dt> <dd>

WWSAPI admite una variedad de opciones de configuración relacionadas con la seguridad. Vea por ejemplo el identificador [**de propiedad de enlace de seguridad \_ \_ \_ \_ de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id). Algunas de estas opciones, como **WS \_ SECURITY BINDING PROPERTY ALLOW ANONYMOUS \_ \_ \_ \_ \_ CLIENTS** permiten a la aplicación reducir el nivel predeterminado de seguridad proporcionado por los distintos enlaces de seguridad. El uso de estas opciones debe evaluarse cuidadosamente para asegurarse de que no haya vectores de ataque resultantes.

Además, como se describió anteriormente, WWSAPI permite que una aplicación deshabilite deliberadamente determinados pasos necesarios para proteger completamente un intercambio de mensajes, como permitir deshabilitar el cifrado aunque se transmitan credenciales de seguridad. Esto permite habilitar determinados escenarios específicos y no debe usarse para la comunicación general. El nivel de protección de [**WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) debe reducirse específicamente para habilitar estos escenarios, y las aplicaciones no deben cambiar ese valor a menos que sea absolutamente necesario, ya que al hacerlo se deshabilitarán muchas comprobaciones diseñadas para garantizar una configuración segura.

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>Almacenamiento de información confidencial en memoria
</dt> <dd>

La información confidencial, como las contraseñas, que se almacena en memoria es vulnerable a ser extraída por un atacante con privilegios mediante, por ejemplo, el archivo de página. WWSAPI realiza una copia de las credenciales proporcionadas y cifra esa copia, dejando los datos originales desprotegidos. Es responsabilidad de la aplicación proteger la instancia original. Además, la copia cifrada se descifra brevemente mientras se usa, lo que abre una ventana para extraerla.

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>Denegación de servicio
</dt> <dd>

El procesamiento de seguridad puede consumir recursos significativos. Cada enlace de seguridad adicional aumenta esos costos. WWSAPI anula el procesamiento de seguridad en cuanto se produce un error de comprobación de seguridad, pero es posible que determinadas comprobaciones, como las decisiones de autorización, no se realicen hasta que se haya realizado un trabajo significativo.

Mientras se procesa un mensaje en el servidor, el estado de seguridad se almacena en el montón de mensajes. La aplicación puede limitar el consumo de memoria durante el procesamiento de seguridad reduciendo el tamaño de ese montón a través de PROPIEDADES DEL MONTÓN DE LA PROPIEDAD DE MENSAJE de \_ \_ \_ \_ WS. Además, ciertos enlaces de seguridad como WS SECURITY CONTEXT MESSAGE SECURITY BINDING pueden hacer que el servidor asigne recursos en \_ \_ nombre del \_ \_ \_ cliente. Los límites de esos recursos se pueden configurar mediante los siguientes valores de id. de propiedad de [**enlace de seguridad \_ \_ \_ \_ de WS:**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)

-   CONTEXTO DE SEGURIDAD MÁXIMO DE CONTEXTOS PENDIENTES DE LA PROPIEDAD DE ENLACE DE SEGURIDAD DE \_ \_ \_ \_ \_ \_ \_ \_ WS
-   CONTEXTOS ACTIVOS MÁXIMOS DE CONTEXTOS ACTIVOS DE LA PROPIEDAD DE ENLACE DE SEGURIDAD DE \_ \_ \_ \_ \_ \_ \_ \_ WS
-   INTERVALO DE RENOVACIÓN \_ DEL CONTEXTO DE SEGURIDAD DE LA PROPIEDAD \_ \_ \_ WS \_ \_ SECURITY BINDING \_
-   WS \_ SECURITY \_ BINDING \_ PROPERTY \_ SECURITY \_ CONTEXT \_ ROLLOVER \_ INTERVAL

Establecer esos límites en valores bajos reduce el consumo máximo de memoria, pero puede provocar que los clientes legítimos se rechacen cuando se alcanza la cuota.

</dd> </dl>

 

 