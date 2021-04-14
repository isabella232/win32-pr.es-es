---
title: Información general sobre seguridad
description: El marco de seguridad de la API de servicios Web de Windows (WWSAPI) proporciona integridad del mensaje, confidencialidad, detección de reproducción y autenticación de servidor mediante la seguridad de transporte.
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- Información general de seguridad de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741e98ef023c0bae146b5fde582484f2dd133df6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488047"
---
# <a name="security-overview"></a>Información general sobre seguridad

El marco de seguridad de la API de servicios Web de Windows (WWSAPI) proporciona:

-   Integridad del mensaje, confidencialidad, detección de reproducción y autenticación de servidor mediante la seguridad de transporte.
-   Autenticación de cliente, como la validación de tokens de seguridad, las comprobaciones de confianza y revocación de certificados, etc. mediante seguridad de mensajes SOAP o seguridad de transporte.

## <a name="the-security-programming-model"></a>Modelo de programación de seguridad

La seguridad está asociada a los [canales de comunicación](channel-layer-overview.md). La protección de un canal consta de los siguientes pasos.

-   Cree e inicialice uno o más [**enlaces de seguridad**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) adecuados para los requisitos de seguridad de la aplicación.
-   Cree una [**Descripción de seguridad**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que contenga esos enlaces de seguridad.
-   Cree un [**canal**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) o [**proxy de servicio**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (en el lado cliente), o cree un [**agente de escucha**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) o un host de [**servicio**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) (en el lado servidor) que pase la descripción de seguridad.
-   Realice los pasos de programación normales del canal de apertura, aceptación, envío, recepción, cierre, etc.

El tiempo de ejecución protege automáticamente los mensajes enviados y recibidos en el canal según la descripción de seguridad proporcionada. Opcionalmente, estos pasos se pueden ajustar mediante la especificación de una o más [Opciones de seguridad de todo el canal](security-channel-settings.md) en la descripción de seguridad o la configuración de seguridad de todo el [enlace](security-binding-settings.md) en un enlace de seguridad.

La aplicación debe realizar cualquier autorización necesaria de identidades de remitente mediante los resultados de [procesamiento de seguridad](security-processing-results.md) adjuntos a cada mensaje recibido. Los pasos de autorización no se especifican en la descripción de seguridad, ni los realiza automáticamente el tiempo de ejecución.

Los errores en la descripción de la seguridad, como los enlaces no admitidos, las propiedades o campos no aplicables, la falta de propiedades o campos obligatorios o los valores de propiedad o campo no válidos provocarán un error en la creación del canal o del agente de escucha.

## <a name="selecting-security-bindings"></a>Selección de enlaces de seguridad

Al diseñar la seguridad de una aplicación, la decisión principal es la selección de los enlaces de seguridad que se van a incluir en la descripción de seguridad. A continuación se indican algunas directrices para elegir los enlaces de seguridad adecuados para el escenario de seguridad de una aplicación. Una heurística útil es comprender primero qué tipos de credenciales de seguridad (por ejemplo, [**certificados X. 509**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential), [**nombres de usuario y contraseñas de dominio de Windows**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential), nombres de usuario y [**contraseñas definidos por la aplicación**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)) estarán disponibles para la aplicación y, a continuación, elegir un enlace de seguridad que pueda usar ese tipo de credencial.

-   La seguridad de transporte, donde la seguridad se aplica en el nivel de secuencia de bytes de transporte (debajo de los límites del mensaje SOAP), es la primera opción que se debe tener en cuenta.
    -   En escenarios de Internet y en los escenarios de intranet en los que se puede implementar un certificado X. 509 en el servidor, la aplicación puede usar el [**\_ enlace de seguridad de \_ transporte \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). En el ejemplo siguiente se muestra esta opción. Cliente: [HttpClientWithSslExample](httpclientwithsslexample.md) Server: [HttpServerWithSslExample](httpserverwithsslexample.md).

        Si se desea la autenticación de cliente a través de la autenticación de encabezado HTTP, se puede Agregar un enlace de seguridad de autenticación de [**\_ \_ encabezado \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) para proporcionar esa funcionalidad.

    -   Para escenarios de intranet en los que los protocolos de autenticación integrada de Windows como Kerberos, NTLM y SPNEGO son adecuados, la aplicación puede usar el [**\_ enlace de \_ \_ \_ seguridad \_ de transporte SSPI TCP de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding). En el ejemplo siguiente se muestra esta opción: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md) Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

        Cliente a través de canalizaciones con nombre: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        Servidor a través de canalizaciones con nombre: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   En el caso de escenarios de equipo local en los que los protocolos de autenticación integrada de Windows como Kerberos, NTLM y SPNEGO son adecuados, la aplicación puede usar el [**\_ enlace de \_ \_ seguridad de transporte \_ \_ SSPI de WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) o el [**enlace de seguridad de transporte de WS \_ NAMEDPIPE \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding). El [**\_ enlace de \_ canal \_ de WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) se prefiere en tales escenarios, ya que garantiza que el tráfico no abandonará el equipo (es la propiedad del **enlace de \_ \_ canal \_ WS NAMEDPIPE**).

-   La seguridad de modo mixto, en la que la seguridad de transporte protege la conexión y un encabezado WS-Security del mensaje SOAP proporciona la autenticación del cliente, es la opción siguiente que se debe tener en cuenta. Los enlaces siguientes se usan junto con uno de los enlaces de seguridad de transporte descritos en la sección anterior.
    -   Cuando el cliente se autentica mediante un par de nombre de usuario/contraseña de nivel de aplicación, la aplicación puede utilizar un [**enlace de seguridad de mensaje de WS \_ username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) para proporcionar los datos de autenticación. En los siguientes ejemplos se muestra el uso de este enlace junto con [**un \_ \_ enlace de \_ seguridad \_ de transporte WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding):
        -   Cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)
        -   Servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)
    -   Cuando el cliente se autentica mediante un vale de Kerberos, la aplicación puede utilizar un [**\_ enlace de \_ \_ seguridad de \_ \_ mensaje WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) para proporcionar los datos de autenticación.
    -   Al utilizar un [contexto de seguridad](security-context.md), el cliente primero establece un contexto de seguridad con el servidor y, a continuación, usa ese contexto para autenticar los mensajes. Para habilitar esta funcionalidad, la descripción de seguridad debe contener [**un \_ \_ enlace de \_ \_ seguridad de \_ mensaje de contexto de WS-Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). Una vez establecido, los contextos de seguridad se pueden transmitir por medio de tokens ligeros, lo que evita tener que enviar las credenciales de cliente potencialmente grandes y costosas de cómputo con cada mensaje.
    -   En un escenario de [seguridad federada](federation.md) , el cliente obtiene primero un token de seguridad emitido por un servicio de token de seguridad (STS) y, a continuación, presenta el token emitido a un servicio. Lado cliente: para obtener el token de seguridad del STS, la aplicación puede usar [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken). Como alternativa, la aplicación puede usar una biblioteca del proveedor de tokens de seguridad del lado cliente como CardSpace o LiveID y, a continuación, utilizar la salida para crear localmente un token de seguridad con [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). En cualquier caso, una vez que el token de seguridad está disponible para el cliente, se puede presentar al servicio mediante una descripción de seguridad que contiene un [**enlace de seguridad de mensaje de token de WS \_ XML \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding). Lado servidor: Si el token de seguridad emitido por el STS es un token SAML, el servidor puede usar una descripción de seguridad con un [**\_ enlace de \_ \_ seguridad \_ de mensaje WS SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding).
        > [!Note]  
        > Windows 7 y Windows Server 2008 R2: WWSAPI solo admite [WS-Trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) y [WS-SecureConversation](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) , tal y como se define en [Lightweight seguridad de servicios web Profile (LWSSP)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Para obtener más información sobre la implementación de Microsoft, consulte la sección sobre la [Sintaxis del mensaje](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) de LWSSP.

         
-   La última opción a tener en cuenta es el uso de enlaces de autenticación sin usar un enlace de protección como el [**\_ enlace de seguridad de \_ transporte \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Esto hará que las credenciales se transmitan en texto no cifrado y puede tener implicaciones de seguridad. El uso de esta opción se debe evaluar cuidadosamente para asegurarse de que no hay ninguna vulnerabilidad. Un ejemplo de uso potencial es intercambiar mensajes entre servidores back-end a través de una red privada segura. Las siguientes configuraciones admiten esta opción.

    -   [**WS \_ El \_ \_ enlace de \_ seguridad \_ de autenticación del encabezado HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) admite esta opción en todas las configuraciones.
    -   [**WS \_ El \_ \_ \_ enlace de seguridad de mensajes de nombre de usuario**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) es compatible con esta opción en el servidor cuando se utiliza http como transporte.
    -   [**WS \_ El \_ \_ enlace de \_ seguridad \_ de mensajes APREQ de Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) admite esta opción en el servidor cuando se utiliza http como transporte.
    -   [**WS \_ El \_ \_ enlace de \_ seguridad \_ de mensaje de contexto de seguridad**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) admite esta opción en el servidor cuando se utiliza http como transporte.
    -   [**WS \_ El \_ \_ \_ enlace de seguridad de mensajes SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) admite esta opción en el servidor cuando se usa http como transporte.

    La habilitación de esta opción requiere establecer explícitamente el [**\_ \_ nivel de protección de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) en un valor distinto del **\_ \_ \_ signo \_ y \_ cifrado del nivel de protección de WS**.

## <a name="channels-and-security"></a>Canales y seguridad

Como se indicó anteriormente, el ámbito de la seguridad es los canales. Además, las operaciones de canal se asignan a los pasos de seguridad de forma coherente en todos los enlaces de seguridad.

-   Creación de canales: el conjunto de enlaces de seguridad especificado en la descripción de seguridad se valida y permanece fijo para el canal a partir de entonces. También se determina la forma de la pila del canal, incluidos los canales secundarios que se usarán para las negociaciones basadas en WS-Trust.
-   Canal abierto: se cargan todas las credenciales que se proporcionan como parte de los enlaces de seguridad y se establecen las sesiones de seguridad. En general, un canal abierto contiene el estado de seguridad "activo". Al abrir un canal de cliente, también se especifica la dirección del punto de conexión del servidor con la que se realizará la autenticación del servidor en tiempo de ejecución.
-   Entre el canal abierto y el cierre: los mensajes se pueden enviar y recibir de forma segura durante esta fase.
-   Envío de mensajes: los tokens de contexto de seguridad se obtienen o se renuevan según sea necesario y se aplica la seguridad a cada mensaje transmitido según la descripción de seguridad. Los errores que se producen al aplicar la seguridad se devuelven a la aplicación como errores de envío.
-   Recepción de mensajes: se comprueba la seguridad de cada mensaje recibido según la descripción de seguridad. Los errores de comprobación de seguridad de los mensajes se devuelven a la aplicación en forma de errores de recepción. Estos errores por mensaje no afectan al estado del canal ni a las recepciones posteriores. La aplicación puede descartar una recepción con errores y reiniciar una recepción para otro mensaje.
-   Anulación de canal: el canal se puede anular en cualquier momento para detener todas las e/s en el canal. Al anular, el canal entrará en un estado de error y no permitirá que se envíen o reciban más. Sin embargo, es posible que el canal siga conservando un estado de seguridad "activo", por lo que será necesario cerrar el canal posteriormente para desechar todo el estado sin problemas.
-   Cerrar canal: el estado de seguridad creado al abrir se desecha y las sesiones se anulan. Los tokens de contexto de seguridad se cancelan. La pila de canales permanece, pero no contiene ningún estado de seguridad "activo" ni credenciales cargadas.
-   Canal libre: se libera la pila de canales creada en la creación, junto con todos los recursos de seguridad.

## <a name="security-apis"></a>API de seguridad

La documentación de la API para la seguridad se agrupa en los temas siguientes.

-   [Descripción de seguridad](security-description.md)
    -   [Configuración del canal de seguridad](security-channel-settings.md)
    -   [Enlaces de seguridad](security-bindings.md)
        -   [Credenciales de seguridad](security-credentials.md)
        -   [Configuración de enlace de seguridad](security-binding-settings.md)
-   [Federación](federation.md)
-   [Contexto de seguridad](security-context.md)
-   [Identidad de extremo](endpoint-identity.md)
-   [Resultados de procesamiento de seguridad](security-processing-results.md)

## <a name="security"></a>Seguridad

Cuando se usa la API de seguridad de WWSAPI, las aplicaciones se encuentran en varios riesgos de seguridad:

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>Configuración involuntaria accidental
</dt> <dd>

WWSAPI admite una variedad de opciones de configuración relacionadas con la seguridad. Vea por ejemplo el identificador de la [**propiedad de enlace de WS \_ \_ \_ \_ Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id). Algunas de estas opciones, como la **propiedad de enlace WS Security, permiten que los \_ \_ \_ \_ \_ \_ clientes anónimos** permitan a la aplicación reducir el nivel de seguridad predeterminado proporcionado por los distintos enlaces de seguridad. El uso de estas opciones debe evaluarse cuidadosamente para asegurarse de que no haya ningún vector de ataque resultante.

Además, como se ha descrito anteriormente, WWSAPI permite a una aplicación deshabilitar deliberadamente determinados pasos necesarios para proteger completamente un intercambio de mensajes, como permitir que deshabilite el cifrado aunque se transmitan credenciales de seguridad. Esto puede habilitar determinados escenarios específicos y no debe usarse para la comunicación general. El [**\_ \_ nivel de protección de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) se debe reducir específicamente para habilitar estos escenarios y las aplicaciones no deben cambiar ese valor a menos que sea absolutamente necesario, ya que si lo hace, se deshabilitarán muchas comprobaciones diseñadas para garantizar una configuración segura.

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>Almacenar información confidencial en memoria
</dt> <dd>

La información confidencial, como contraseñas, que se almacena en la memoria es vulnerable a la extracción por un atacante con privilegios por medio de, por ejemplo, el archivo de paginación. WWSAPI realiza una copia de las credenciales proporcionadas y cifra esa copia, lo que deja los datos originales desprotegidos. Es responsabilidad de la aplicación proteger la instancia original. Además, la copia cifrada se descifra brevemente mientras se usa, abriendo una ventana para extraerla.

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>Denegación de servicio
</dt> <dd>

El procesamiento de seguridad puede consumir importantes recursos. Cada enlace de seguridad adicional aumenta los costos. WWSAPI anula el procesamiento de seguridad en cuanto se encuentra un error de comprobación de seguridad, pero es posible que ciertas comprobaciones, como las decisiones de autorización, no tengan lugar hasta que se haya realizado un trabajo significativo.

Mientras se procesa un mensaje en el servidor, el estado de seguridad se almacena en el montón de mensajes. La aplicación puede limitar el consumo de memoria durante el procesamiento de seguridad reduciendo el tamaño del montón a través de \_ \_ las propiedades del montón de propiedades del mensaje de WS \_ \_ . Además, algunos enlaces de seguridad, como el \_ \_ \_ \_ enlace de seguridad de mensaje de contexto de WS Security, \_ pueden hacer que el servidor asigne recursos en nombre del cliente. Los límites de esos recursos se pueden configurar por medio de los siguientes valores de [**identificador de propiedad de enlace de WS \_ Security \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) :

-   \_ \_ \_ \_ \_ \_ \_ contextos pendientes de contexto de seguridad \_ de la propiedad de enlace de WS Security
-   \_ \_ \_ \_ \_ \_ contextos activos máximos del contexto de \_ seguridad \_ de la propiedad de enlace de WS-Security
-   \_intervalo de \_ \_ renovación del \_ \_ contexto de \_ seguridad \_ de la propiedad de enlace de WS Security
-   \_intervalo de \_ \_ sustitución del \_ \_ contexto de \_ seguridad \_ de la propiedad de enlace de WS Security

El establecimiento de estos límites en valores bajos reduce el consumo máximo de memoria, pero puede dar lugar a clientes legítimos que se rechazan cuando se alcanza la cuota.

</dd> </dl>

 

 