---
title: Secuencia de llamadas API del método Authenticator
description: Obtenga información sobre la secuencia de llamadas API del método Authenticator. Vea una lista que muestra la secuencia de llamadas realizadas por un EAPHost en un método de autenticación de EAP.
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bb5c7d64bfe6e38ebb97550dc76fe8ffcae8176
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421416"
---
# <a name="authenticator-method-api-call-sequence"></a>Secuencia de llamadas API del método Authenticator

En este tema se proporciona la secuencia de llamadas específica para la API del método Authenticator. Durante una sesión de autenticación EAP típica, EAPHost realiza varias llamadas en un método EAP que implementa las API del método de autenticador de EAPHost.

En la siguiente lista se muestra la secuencia de llamadas realizadas por EAPHost en un método de autenticación de EAP.

-   El autenticador de EAP carga primero el archivo DLL de método EAP que se usa para la autenticación específica en un servidor de directivas de redes (NPS) u otro servidor de autenticación.
-   Llama a [**EapAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) en el método con una estructura de [**\_ tipo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type) rellenada para obtener una lista de punteros a las funciones implementadas en el archivo dll. Se supone que las llamadas a funciones subsiguientes de los métodos de autenticador (servidor) se implementan en el archivo DLL.
-   Llama a [**EapAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) para indicar a la biblioteca de métodos EAP que debe prepararse para al menos una sesión de autenticación mediante este método de autenticador.
-   Llama a [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) para establecer una sesión de autenticación única.
-   Repite los pasos siguientes hasta que [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) indica que hay un resultado de autenticación disponible.
    -   Llama a [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) con un puntero a un paquete de solicitud que se va a pasar al suplicante.
    -   Llama a [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) para recuperar el paquete de respuesta enviado por el solicitante. Esta función devuelve un código de **\_ acción de \_ \_ respuesta \_ del autenticador de método EAP** que indica la siguiente acción que el autenticador debe realizar en la sesión de autenticación EAP.
    -   Si el código de acción [es \_ \_ respuesta del autenticador del método \_ \_ EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), indica que el método EAP tiene atributos disponibles para que el autenticador recupere y pase al método del mismo nivel. El autenticador llama a [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) para obtener los distintos atributos de autenticación EAP del método de autenticador EAP. Después de que el autenticador procese los atributos, llama a [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) , que proporciona los atributos de autenticación EAP actualizados para establecer en el método de autenticación de EAP. Esta función devuelve un código de **\_ acción de \_ \_ respuesta \_ del autenticador de método EAP** que determina la acción subsiguiente.
-   Si el código de acción es el resultado de la [ \_ \_ \_ respuesta \_ del autenticador del método EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), indica que el autenticador ha determinado los resultados de la sesión de autenticación y que los resultados están disponibles para EAPHost. El autenticador llama a [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) y obtiene los resultados de la sesión de autenticación.
-   Esto va seguido de una llamada a [**EapMethodAuthenticatorEndSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) para finalizar la sesión de autenticación.
-   Por último, se realiza una llamada a [**EapMethodAuthenticatorShutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) para descargar el archivo DLL del método Authenticator.
-   Descarga la biblioteca de métodos EAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_acción de \_ respuesta del autenticador del método EAP \_ \_**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[Secuencia de llamadas API de suplicante](supplicant-api-call-sequence.md)
</dt> <dt>

[Secuencia de llamadas API de método del mismo nivel](peer-method-api-call-sequence.md)
</dt> <dt>

[Secuencias de llamadas de EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




