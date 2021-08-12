---
title: Tunnel Secuencia de llamadas api de método
description: Obtenga información sobre la secuencia de llamadas API para Tunnel métodos. Consulte información general y vea recursos adicionales disponibles.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca32a889229b6cdbdb3f008ebea8b838f9b6d64fba36bc2a30c4ddd9d62ac83d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272802"
---
# <a name="tunnel-method-api-call-sequence"></a>Tunnel Secuencia de llamadas api de método

En este tema se trata la secuencia de llamadas API para Tunnel Métodos

## <a name="tunnel-method-call-sequence-overview"></a>Tunnel Introducción a la secuencia de llamadas de método

Cuando Supplicant obtiene la solicitud de datos de usuario y de identidad de usuario, normalmente se produce el siguiente flujo de llamada API.

-   El supplicant llama a EapHostPeerProcessReceivedPacket en EapHost para procesar el paquete recibido del autenticador.
-   Tras procesar este paquete, EAPHost lo determina como paquete IdentityRequest y llama a [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) en el método de túnel para obtener la identidad de usuario que se usará para la autenticación.
-   Si el método tunnel necesita obtener la identidad del usuario del método interno, llama a [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) en EAPHost interno, que a su vez llama a [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) en el método interno.

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>Interacción del usuario con la Tunnel API Flow

En determinados casos, cuando la identidad no está disponible o cuando el usuario debe proporcionar información adicional, el método Eap genera un cuadro de diálogo de interfaz de usuario en el suplicante.

En tales casos, la siguiente secuencia de llamadas suele tener lugar para obtener información directamente del usuario.

-   Tunnel El método eap devuelve código de acción para invocar la interfaz de usuario a EapHost. Supplicant llama [**a EapHostPeerGetUIContext para**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)obtener la información de contexto de la interfaz de usuario actual para el cuadro de diálogo de interfaz de usuario.
-   A continuación, Supplicant [ **llama a EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) Esta función usa la información de contexto de la interfaz de usuario para generar una interfaz de usuario interactiva que se usa para obtener información de credenciales del usuario. El proceso de interfaz Eappcfg.dll carga y obtiene los punteros a EapPeerInvokeInteractiveUI y EapPeerFreeMemory.
    > [!Note]  
    > Normalmente, el proceso de interfaz de usuario recopila la interfaz de usuario o controla la interfaz de usuario interactiva y es independiente del proceso de suplicación. Separar los dos procesos no es un requisito de EAPHost, pero hacerlo tiene la ventaja de permitir que el proceso de interfaz de usuario interactúe con el escritorio.

     

-   EapHost llama a [**EapPeerInvokeIdentityUI en el**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) método tunnel para obtener información de identidad del usuario.
-   Para obtener la identidad del usuario del método interno, el método tunnel llama a [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) en EAPHost interno.
-   EAPHost interno llama [**a EapPeerInvokeIdentityUI en el**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) método interno para invocar la interfaz de usuario de identidad de usuario.
-   [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) proporciona una información de contexto de interfaz de usuario nueva o actualizada al método del mismo nivel de EAP cargado en EAPHost después de que se haya producido la interfaz de usuario.

En el diagrama siguiente se explica la secuencia de llamadas API para Tunnel métodos

![secuencia de llamadas api de métodos de túnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencia de llamadas de EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Secuencia de llamadas de API suplicante](supplicant-api-call-sequence.md)
</dt> <dt>

[Referencia de API de EAPHost Supplicant](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




