---
title: Secuencia de llamadas api del método del mismo nivel
description: Obtenga información sobre la secuencia de llamadas API del método del mismo nivel. Vea una lista que muestra la secuencia de llamadas realizadas por eapHost en un método del mismo nivel de EAP.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647a6a558d282ff4ae3691c23600b696b79764ee68a1007ccabb445c5a1fe65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042793"
---
# <a name="peer-method-api-call-sequence"></a>Secuencia de llamadas api del método del mismo nivel

En este tema se proporciona la secuencia de llamadas específica para la API del método del mismo nivel. Durante una sesión de autenticación eap típica, EAPHost realiza una serie de llamadas en métodos EAP para implementar la API del método del mismo nivel eapHost.

En la lista siguiente se muestra la secuencia de llamadas realizadas por EAPHost en un método del mismo nivel de EAP.

-   Carga el archivo DLL del método del mismo nivel de EAP utilizado para la autenticación.
-   Llama [**a EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) en el método para obtener una lista de punteros a funciones implementadas en el archivo DLL. Se supone que las llamadas de función posteriores por el par EAPHost (cliente) se implementan en el archivo DLL.
-   Llama [**a EapPeerInitialize para**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) indicar a la biblioteca de métodos eap que se prepare para al menos una sesión de autenticación mediante este método del mismo nivel.
-   Llama a [**EapPeerBeginSession para**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) establecer una sesión de autenticación única.
-   Llama [**a EapPeerGetIdentity para**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) obtener la identidad que se usará para la autenticación. Si la identidad no está disponible o si el usuario debe proporcionar información adicional, EAPHost llama a [ **EapPeerGetUIContext.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Esta función obtiene la información de contexto para el cuadro de diálogo de la interfaz de usuario que se va a generar en el suplicante. Una vez que el usuario ha enviado la información de identidad, la identidad del usuario se establece con una llamada a [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)y se obtiene mediante una llamada a **EapPeerGetIdentity**.
-   Repite los pasos siguientes hasta que [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) indica que hay disponible un resultado de autenticación.
    -   Llama [**a EapPeerProcessRequestPacket con**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) el puntero de un paquete de solicitud para pasar al suplicante.
    -   Llama **a EapPeerGetResponsePacket para** recuperar el paquete de respuesta que se va a enviar al autenticador.
    -   Opcionalmente, si los atributos de EAP deben recuperarse o enviarse durante la sesión de autenticación, EAPHost llama a [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) y [**EapPeerSetResponseAttributes,**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) respectivamente.
-   Cuando el autenticador envía un código de acción que indica que la autenticación se ha completado, EAPHost llama a [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) y obtiene los resultados de la autenticación.
-   Llama [**a EapPeerEndSession para**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) finalizar la sesión de autenticación.
-   Llama [**a EapPeerShutdown para**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) descargar el archivo DLL del método del mismo nivel.
-   Descarga la biblioteca de métodos EAP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencia de llamadas de API suplicante](supplicant-api-call-sequence.md)
</dt> <dt>

[Authenticator Secuencia de llamadas api de método](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Secuencias de llamadas EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




