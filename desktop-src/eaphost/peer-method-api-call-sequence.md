---
title: Secuencia de llamadas API de método del mismo nivel
description: Obtenga información sobre la secuencia de llamadas API del método del mismo nivel. Vea una lista que muestra la secuencia de llamadas realizadas por un EAPHost en un método EAP del mismo nivel.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac9be0f6de228fd5b1ebf2d2c28320baf76e914
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149630"
---
# <a name="peer-method-api-call-sequence"></a>Secuencia de llamadas API de método del mismo nivel

En este tema se proporciona la secuencia de llamadas específica para la API del método del mismo nivel. Durante una sesión de autenticación EAP típica, EAPHost realiza varias llamadas en métodos EAP para implementar la API de método del mismo nivel de EAPHost.

En la siguiente lista se muestra la secuencia de llamadas realizadas por EAPHost en un método EAP del mismo nivel.

-   Carga el archivo DLL de método EAP del mismo nivel que se usa para la autenticación.
-   Llama a [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) en el método para obtener una lista de punteros a las funciones implementadas en el archivo dll. Se supone que las llamadas a funciones posteriores realizadas por el homólogo (cliente) de EAPHost se implementan en el archivo DLL.
-   Llama a [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) para indicar a la biblioteca de métodos EAP que debe prepararse para al menos una sesión de autenticación mediante este método del mismo nivel.
-   Llama a [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) para establecer una sesión de autenticación única.
-   Llama a [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) para obtener la identidad que se va a usar para la autenticación. Si la identidad no está disponible, o si el usuario debe proporcionar información adicional, EAPHost llama a [ **EapPeerGetUIContext.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Esta función obtiene la información de contexto para el cuadro de diálogo de la interfaz de usuario que se generará en el suplicante. Una vez que el usuario ha enviado la información de identidad, la identidad del usuario se establece con una llamada a [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)y se obtiene mediante una llamada a **EapPeerGetIdentity**.
-   Repite los pasos siguientes hasta que [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) indica que hay un resultado de autenticación disponible.
    -   Llama a [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) con el puntero de un paquete de solicitud que se va a pasar al suplicante.
    -   Llama a **EapPeerGetResponsePacket** para recuperar el paquete de respuesta que se va a enviar al autenticador.
    -   Opcionalmente, si es necesario recuperar o enviar atributos EAP durante la sesión de autenticación, EAPHost llama a [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) y [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) , respectivamente.
-   Cuando el autenticador envía un código de acción que indica que se ha completado la autenticación, EAPHost llama a [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) y obtiene los resultados de la autenticación.
-   Llama a [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) para finalizar la sesión de autenticación.
-   Llama a [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) para descargar el archivo DLL del método del mismo nivel.
-   Descarga la biblioteca de métodos EAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencia de llamadas API de suplicante](supplicant-api-call-sequence.md)
</dt> <dt>

[Secuencia de llamadas API del método Authenticator](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Secuencias de llamadas de EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




