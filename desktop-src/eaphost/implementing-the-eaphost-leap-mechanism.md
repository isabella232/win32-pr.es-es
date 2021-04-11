---
title: Implementación del mecanismo LEAP de EAPHost
description: Describe el mecanismo de EAPHost que permite a terceros escribir módulos de protocolo de autenticación extensible ligero (LEAP) para Windows.
ms.assetid: d17a99cb-4a43-4719-984e-b742c9518f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc50cda8d32cc26dd81af5733345deebb579c792
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104149707"
---
# <a name="implementing-the-eaphost-leap-mechanism"></a>Implementación del mecanismo LEAP de EAPHost

En este tema se describe el mecanismo de EAPHost que permite a terceros escribir módulos de protocolo de autenticación extensible ligero (LEAP) para Windows. LEAP es un método de autenticación heredado, creado por Cisco, según [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016). Para obtener más información sobre LEAP, consulte [Cisco Leap Q&A](https://go.microsoft.com/fwlink/p/?linkid=84018).

## <a name="eaphost-authentication-process"></a>Proceso de autenticación de EAPHost

El proceso de autenticación de EAPHost normal se produce de la manera siguiente:

-   El autenticador envía una solicitud para autenticar el elemento del mismo nivel. Por ejemplo, la aplicación llama a [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con los datos de usuario y la configuración de EAPHost.
-   El elemento del mismo nivel envía un paquete de respuesta en respuesta a una solicitud válida. Por ejemplo, una llamada correcta devuelve un identificador de sesión de **\_ \_ identificador de sesión EAP** .
-   El autenticador envía un paquete de solicitud adicional y el elemento del mismo nivel responde con una respuesta. Por ejemplo, la aplicación llama a [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) para obtener paquetes EAP recibidos por EAPHost a lo largo de la sesión. Cada paquete se procesa mediante una llamada a [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket).
-   [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) siempre devolverá un código de acción. A continuación, el suplicante debe llamar a la función correspondiente al código de acción.
-   La secuencia de solicitudes y respuestas continúa siempre y cuando sea necesario. Por ejemplo, la aplicación puede llamar a [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) para solicitar los atributos EAP disponibles y el elemento del mismo nivel responde con [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) para devolverlos.
-   Después de una solicitud inicial, no se puede enviar una nueva solicitud hasta que se reciba una respuesta válida.
-   La conversación continúa hasta que el autenticador no puede autenticar al mismo nivel, en cuyo caso la implementación del autenticador debe transmitir un error de EAP. Por ejemplo, las respuestas inaceptables a una o más solicitudes harían que el autenticador transmitiera un error de EAP de código 4.
-   Como alternativa, la conversación de autenticación puede continuar hasta que el autenticador determine que se ha producido la autenticación correcta, en cuyo caso el autenticador debe transmitir un EAP correcto (código 3).
-   Si el resultado indica éxito o error, la aplicación llama a [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) para finalizar la sesión. En caso de error, se puede intentar volver a realizar la autenticación abriendo otra sesión con EAPHost y proporcionando la misma identidad o una nueva.

### <a name="leap-authentication-process"></a>Proceso de autenticación LEAP

El proceso de autenticación LEAP difiere del proceso de autenticación de EAPhost normal de la siguiente manera:

-   El servidor inicia la autenticación EAP (autenticador). Por el contrario, el cliente (del mismo nivel) inicia LEAP.
    -   Por lo tanto, al escribir un módulo LEAP, siempre debe asegurarse de que el paquete de solicitud de desafío desde el método del mismo nivel y la respuesta EAP desde el servidor EAP siempre deben tener el mismo identificador de paquete que el paquete de EAP correcto del servidor.

    <!-- -->

    -   Por el contrario, los paquetes de solicitud y respuesta y correctos de EAPHost suelen tener identificadores diferentes.
        > [!Note]  
        > Cada solicitud EAP tiene un campo de tipo para indicar lo que se solicita. Al igual que con el paquete de solicitud, cada paquete de respuesta EAP contiene un campo de tipo, que se corresponde con el campo de tipo de la solicitud. Algunos ejemplos son los paquetes de solicitud de identidad y de solicitud de desafío.

         

-   En el caso de que se produzca un error con EAPHost, se puede intentar la reautenticación abriendo otra sesión con EAPHost y proporcionando la misma identidad o una nueva identidad.

### <a name="leap-authenticator-method-implementation"></a>Implementación del método de autenticador LEAP

Al desarrollar un método de autenticador LEAP, asegúrese de lo siguiente:

-   Los métodos de autenticación LEAP deben devolver el código de acción de [**\_ envío de \_ \_ respuesta \_ del autenticador del método EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) después de la primera fase de autenticación (autenticación del mismo nivel) se realiza correctamente. Después, cuando se llama a [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) , debe devolver un [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket) válido con un código EAP de [**EapCodeSuccess**](/windows/win32/api/eapmethodtypes/ne-eapmethodtypes-eapcode).
-   Los métodos de autenticación LEAP deben devolver el código de acción de [**\_ resultado de \_ \_ respuesta \_ del autenticador del método EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) si la primera fase de la autenticación del mismo nivel no se realiza correctamente.
-   Los métodos de autenticador LEAP deben devolver el paquete de respuesta de autenticación final con el código de acción de [**resultado de \_ \_ \_ respuesta \_ del autenticador del método EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) cuando se llama a [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) . A continuación, en las llamadas posteriores a [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) , se debe devolver el **\_ \_ identificador de sesión EAP** para identificar la sesión autenticada.
-   

### <a name="leap-peer-method-implementation"></a>Implementación del método del mismo nivel LEAP

Al desarrollar un método del mismo nivel LEAP, asegúrese de lo siguiente:

-   Los métodos del mismo nivel LEAP deben devolver el código de acción [**EapPeerMethodResponseActionSend**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) después de la primera fase de autenticación (autenticación del mismo nivel) se realiza correctamente.
-   Los métodos del mismo nivel LEAP deben devolver el código de acción [**EapPeerMethodResponseActionResult**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) después de que la segunda fase de autenticación se realice correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencia de llamadas de EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> </dl>

 

 




