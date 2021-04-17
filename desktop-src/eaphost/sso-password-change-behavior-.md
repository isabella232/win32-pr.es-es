---
title: Comportamiento de cambio de contraseña de SSO
description: Proporciona un enfoque paso a paso para resolver el comportamiento del cambio de contraseña de SSO.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105665767"
---
# <a name="sso-password-change-behavior"></a>Comportamiento de cambio de contraseña de SSO

En este tema se proporciona un enfoque paso a paso para resolver el comportamiento del cambio de contraseña de SSO.

## <a name="step-by-step-approach"></a>Enfoque paso a paso

La lista siguiente representa un enfoque paso a paso para resolver el comportamiento del cambio de contraseña de SSO.

-   Una vez que el método EAP recibe una notificación sobre un cambio de contraseña, el método notifica a EAPHost; A su vez, EAPHost notifica al solicitante devolviendo el código de acción [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   Después de recibir el código de acción [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) de EAPHost, el solicitante obtiene el contexto de la interfaz de usuario del método EAP mediante una llamada a la función [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) . A continuación, EAPHost obtiene el contexto de la interfaz de usuario del método EAP mediante una llamada a la función de método correspondiente.
-   El suplicante pasa el contexto de la interfaz de usuario al proceso de la interfaz de usuario (mediante algún tipo de comunicación entre procesos).
-   El proceso de la interfaz de usuario llama a [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) en EAPHost.
-   EAPHost recopila el contexto de la interfaz de usuario mediante una llamada a [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) en el método EAP.
-   El método EAP proporciona cualquier información de contexto de la interfaz de usuario necesaria en la estructura de [**datos de interfaz de \_ \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , donde *DwDataType* se establece en *EapCredExpiryReq* y *pbUiData* apunta a una estructura de tipo [**\_ \_ req de credenciales de EAP**](eap-cred-req.md).
-   Al rellenar la estructura de datos de la [**\_ interfaz de \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , este método EAP solo rellenará el parámetro *curCreds* y no establecerá la marca de [**\_ \_ \_ \_ \_ \_ solo lectura del campo de entrada de la interfaz de usuario EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) en la estructura de **\_ \_ \_ \_ datos del campo de entrada de configuración de EAP** .
    > [!Note]  
    > La marca de [**\_ \_ \_ \_ \_ \_ solo lectura del campo de entrada**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) de la interfaz de usuario de EAP es para los campos de miembro que deben cambiarse.

     

-   Tras recopilar el contexto de la interfaz de usuario informtion, el proceso de IU representa una interfaz de usuario para recopilar información de cambio de contraseña del usuario. Esta información se rellena en el parámetro *NewCreds* de la estructura del [**\_ \_ \_ req de expiración**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) de la credencial de EAP.
-   El proceso de la interfaz de usuario vuelve a pasar la estructura de [**\_ \_ resp de EAP**](eap-cred-resp.md) a EAPHost a través de [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).
-   El proceso de IU pasa este BLOB de usuario al suplicante y el suplicante continúa con las funciones de tiempo de ejecución de EAPHost como de costumbre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escenarios de EAPHost de SSO](why-eaphost-sso.md)
</dt> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




