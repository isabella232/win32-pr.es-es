---
title: Authenticator Secuencia de llamadas api de método
description: Obtenga información sobre la secuencia de llamadas API del método autenticador. Vea una lista que muestra la secuencia de llamadas realizadas por un EAPHost en un método autenticador de EAP.
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3864d7b08c3c5c154ef3be86d0ac14716cd8b46adb1485fc5c55e598f870a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852295"
---
# <a name="authenticator-method-api-call-sequence"></a>Authenticator Secuencia de llamadas api de método

En este tema se proporciona la secuencia de llamadas específica para la API del método autenticador. Durante una sesión de autenticación EAP típica, EAPHost realiza una serie de llamadas en un método EAP que implementan las API del método autenticador EAPHost.

En la lista siguiente se muestra la secuencia de llamadas realizadas por EAPHost en un método autenticador de EAP.

-   El autenticador EAP carga primero el archivo DLL del método EAP usado para la autenticación específica en un servidor de directivas de red (NPS) u otro servidor de autenticación.
-   Llama a [**EapAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) en el método con una estructura [**DE TIPO \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type) rellena para obtener una lista de punteros a funciones implementadas en el archivo DLL. Se supone que las llamadas a funciones posteriores por los métodos autenticadores (servidor) se implementan en el archivo DLL.
-   Llama [**a EapAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) para indicar a la biblioteca de métodos EAP que se prepare para al menos una sesión de autenticación mediante este método autenticador.
-   Llama a [**EapMethodAuthenticatorBeginSession para**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) establecer una sesión de autenticación única.
-   Repite los pasos siguientes hasta [**que EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) indica que hay disponible un resultado de autenticación.
    -   Llama [**a EapMethodAuthenticatorSendPacket con**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) un puntero a un paquete de solicitud para pasar al suplicante.
    -   Llama [**a EapMethodAuthenticatorReceivePacket para**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) recuperar el paquete de respuesta enviado por el suplicante. Esta función devuelve un código **EAP METHOD AUTHENTICATOR RESPONSE \_ \_ \_ \_ ACTION** que indica la siguiente acción que el autenticador debe realizar en la sesión de autenticación eap.
    -   Si el código de acción es [EAP METHOD AUTHENTICATOR RESPONSE \_ \_ \_ \_ RESPOND](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), indica que el método EAP tiene atributos disponibles para que el autenticador recupere y pase al método del mismo nivel. Authenticator a [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) para obtener los distintos atributos de autenticación eap del método autenticador eap. Una vez que el autenticador procesa los atributos, llama a [**EapMethodAuthenticatorSetAttributes,**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) que proporciona atributos de autenticación EAP actualizados para establecer en el método autenticador eap. Esta función devuelve un código **EAP METHOD AUTHENTICATOR RESPONSE \_ \_ \_ \_ ACTION** que determina la acción posterior.
-   Si el código de acción es [EAP METHOD AUTHENTICATOR RESPONSE \_ \_ \_ \_ RESULT](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), indica que el autenticador ha determinado los resultados de la sesión de autenticación y esos resultados están disponibles para EAPHost. Authenticator llama [**a EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) y obtiene los resultados de la sesión de autenticación.
-   Esto va seguido de una llamada a [**EapMethodAuthenticatorEndSession para**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) finalizar la sesión de autenticación.
-   Por último, se realiza una llamada [**a EapMethodAuthenticatorShutdown para**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) descargar el archivo DLL del método autenticador.
-   Descarga la biblioteca de métodos EAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ACCIÓN DE \_ RESPUESTA \_ DEL AUTENTICADOR DEL MÉTODO \_ \_ EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[Secuencia de llamadas api de suplicación](supplicant-api-call-sequence.md)
</dt> <dt>

[Secuencia de llamadas api del método del mismo nivel](peer-method-api-call-sequence.md)
</dt> <dt>

[Secuencias de llamadas eaphost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




