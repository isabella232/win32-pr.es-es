---
title: Secuencia de llamadas API de método de túnel
description: Obtenga información sobre la secuencia de llamada de API para los métodos de túnel. Vea información general y ver recursos adicionales disponibles.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359430"
---
# <a name="tunnel-method-api-call-sequence"></a>Secuencia de llamadas API de método de túnel

En este tema se trata la secuencia de llamadas API para los métodos de túnel

## <a name="tunnel-method-call-sequence-overview"></a>Información general sobre la secuencia de llamadas al método de túnel

Cuando el solicitante recibe solicitudes de identidad de usuario y datos de usuario, normalmente se produce el siguiente flujo de llamadas de API.

-   El solicitante llama a EapHostPeerProcessReceivedPacket en EapHost para procesar el paquete recibido del autenticador.
-   Al procesar este paquete, EAPHost lo determina como paquete IdentityRequest y llama a [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) en el método de túnel para obtener la identidad del usuario que se va a usar para la autenticación.
-   Si el método de túnel necesita obtener la identidad del usuario del método interno, llama a [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) en EAPHost interno, que a su vez llama a [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) en el método interno.

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>Interacción del usuario con el flujo de llamadas de API de métodos de túnel

En algunos casos, cuando la identidad no está disponible o cuando el usuario debe proporcionar información adicional, el método EAP genera un cuadro de diálogo de interfaz de usuario en el suplicante.

En estos casos, la siguiente secuencia de llamadas tiene lugar normalmente para obtener información directamente del usuario.

-   El método EAP de túnel devuelve el código de acción para invocar la interfaz de usuario a EapHost. El solicitante llama a [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)para obtener la información de contexto de la interfaz de usuario actual para el cuadro de diálogo de la interfaz de usuario.
-   Después, el suplicante llama a [ **EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) Esta función usa la información de contexto de la interfaz de usuario para generar una interfaz de usuario interactiva que se usa para obtener información de credenciales del usuario. El proceso de la interfaz de usuario carga Eappcfg.dll y obtiene los punteros a EapPeerInvokeInteractiveUI y EapPeerFreeMemory.
    > [!Note]  
    > Normalmente, el proceso de la interfaz de usuario recopila la interfaz de usuario o controla la interfaz de usuario interactiva y es independiente del proceso del suplicante. La separación de los dos procesos no es un requisito de EAPHost, pero esto tiene la ventaja de permitir que el proceso de la interfaz de usuario interactúe con el escritorio.

     

-   EapHost llama a [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) en el método de túnel para obtener información de identidad del usuario.
-   Para obtener la identidad del usuario desde el método interno, el método de túnel llama a [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) en EAPHost interno.
-   EAPHost interno llama a [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) en el método interno para invocar la interfaz de usuario de identidad del usuario.
-   [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) proporciona información de contexto de la interfaz de usuario nueva o actualizada para el método EAP del mismo nivel cargado en EAPHost después de que se haya generado la interfaz de usuario.

En el diagrama siguiente se explica la secuencia de llamadas API para los métodos de túnel

![secuencia de llamadas API de métodos de túnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencia de llamadas de EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Secuencia de llamadas API de suplicante](supplicant-api-call-sequence.md)
</dt> <dt>

[Referencia de API suplicante de EAPHost](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




