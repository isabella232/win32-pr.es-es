---
title: Secuencia de llamadas API de suplicante
description: Obtenga información sobre la secuencia de llamadas a la API del suplicante. Vea información general de la secuencia de llamadas y ver recursos adicionales disponibles.
ms.assetid: 83276783-aee5-43ac-982d-1144df982a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c93afea6dbf4c3220bbeaec4f6278eb3d0b756
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995645"
---
# <a name="supplicant-api-call-sequence"></a>Secuencia de llamadas API de suplicante

En este tema se proporciona la secuencia de llamadas específica para la API del suplicante.

## <a name="supplicant-api-call-sequence-overview"></a>Introducción a la secuencia de llamadas API de suplicante

Cuando el solicitante recibe un paquete EAP de un proveedor, como un punto de acceso, normalmente se produce el siguiente flujo de llamadas API de suplicante.

-   La aplicación llama a [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con datos de configuración y datos de usuario de EAPHost. Una llamada correcta devuelve un identificador de sesión de **\_ \_ identificador de sesión EAP** .
-   Cada paquete recibido por el solicitante se procesa mediante una llamada a [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket). A continuación, el suplicante llama a la función correspondiente al código de acción devuelto por la función.
-   Si el código de acción es **EapHostPeerResponseSend**, el solicitante llama a [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) para obtener la respuesta que se va a enviar al autenticador.
-   Si durante la sesión, el código de acción devuelto al suplicante es **EapHostPeerResponseRespond**, indica que los atributos de EAP están disponibles. A continuación, el suplicante llama a [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) para obtenerlos. Estos atributos contienen datos complementarios que se usan durante el proceso de autenticación. Después de que el suplicante complete el procesamiento de los atributos, llama a [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) , que actualiza los datos. Esta función devuelve un código de acción que determina la siguiente acción del suplicante.
-   Si el código de acción es **EapHostPeerResponseInvokeUI** , el solicitante genera un cuadro de diálogo de interfaz de usuario para obtener datos interactivos del usuario, como credenciales o información de identidad. Consulte interacción del usuario con el flujo de llamadas de la API de suplicante a continuación.
-   Si el código de acción es **EapHostPeerResponseResult**, indica que los resultados de la sesión de autenticación están disponibles para el solicitante. A continuación, el suplicante llama a [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult) para obtener los resultados. Independientemente de si los resultados indican éxito o error, el solicitante llama a [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession). En caso de error, se puede intentar volver a realizar la autenticación abriendo otra sesión con EAPHost y proporcionando una nueva identidad o intentando de nuevo la autenticación con la identidad original.

## <a name="user-interaction-with-the-supplicant-api-call-flow"></a>Interacción del usuario con el flujo de llamadas de la API del suplicante

En algunos casos, el solicitante debe obtener información del usuario para continuar con el proceso de autenticación.

En la siguiente lista se muestra la secuencia de llamadas en el suplicante y el proceso de IU de EAPHost necesarios para habilitar la entrada interactiva.

1.  El suplicante obtiene el contexto de la interfaz de usuario actual llamando a [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext).
2.  Después, el solicitante envía los datos de contexto de la interfaz de usuario al proceso de la interfaz de usuario del suplicante.
    > [!Note]  
    > El proceso de la interfaz de usuario, que normalmente recopila la interfaz de usuario o controla la interfaz de usuario interactiva, es independiente del proceso del suplicante. La separación de los dos procesos no es un requisito de EAPHost, pero esto tiene la ventaja de permitir que el proceso de la interfaz de usuario interactúe con el escritorio.

     

3.  Si el suplicante desea representar la interfaz de usuario por sí misma, llama a la función [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) para obtener los campos de entrada para que se produzcan los componentes de interfaz de usuario interactiva. De lo contrario, sigue el modelo tradicional de invocar la interfaz de usuario interactiva mediante una llamada a [ **EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)
    > [!Note]  
    > Si se devuelve la [**\_ operación de método EAPHOST de EAP E \_ \_ \_ \_ no \_ compatible**](eap-related-error-and-information-constants.md) , el suplicante debe seguir el modelo tradicional de invocar la interfaz de usuario interactiva de método llamando a [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui). Si se produce un error, [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) devolverá un código de retorno distinto de **null**.

     

4.  Si el solicitante llama a [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) o [**EaphostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) , el proceso de la interfaz de usuario pasa los datos de contexto existentes y carga Eappcfg.dll. Se genera una interfaz de usuario adecuada para recopilar los datos nuevos. Los nuevos datos de contexto de la interfaz de usuario, que ahora pueden contener datos proporcionados por el usuario, se copian y los datos de contexto anteriores se liberan con una llamada a [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory).
5.  El proceso de la interfaz de usuario devuelve los nuevos datos de contexto al suplicante, que llama a [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) para establecerlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencia de llamadas API de método del mismo nivel](peer-method-api-call-sequence.md)
</dt> <dt>

[Secuencia de llamadas API del método Authenticator](authenticator-method-api-call-sequence.md)
</dt> <dt>

[Secuencia de llamadas de EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Suplicantes de EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




