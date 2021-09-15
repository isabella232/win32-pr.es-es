---
title: Comportamiento de cambio de contraseña de SSO
description: Proporciona un enfoque paso a paso para resolver el comportamiento de cambio de contraseña de SSO.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473223"
---
# <a name="sso-password-change-behavior"></a>Comportamiento de cambio de contraseña de SSO

En este tema se proporciona un enfoque paso a paso para resolver el comportamiento de cambio de contraseña de SSO.

## <a name="step-by-step-approach"></a>Enfoque paso a paso

En la lista siguiente se representa un enfoque paso a paso para resolver el comportamiento de cambio de contraseña de SSO.

-   Una vez que se notifica al método EAP sobre un cambio de contraseña, el método notifica a EAPHost; EAPHost a su vez notifica al suplicante devolviendo el código de acción, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   Después de recibir el código de acción [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) de EAPHost, el suplicante obtiene el contexto de la interfaz de usuario del método EAP mediante una llamada a la [**función EapHostPeerGetUIContext.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) EAPHost obtiene a continuación el contexto de la interfaz de usuario del método EAP mediante una llamada a la función de método correspondiente.
-   El suplicante pasa el contexto de la interfaz de usuario al proceso de la interfaz de usuario (mediante algún tipo de comunicación entre procesos).
-   El proceso de interfaz de [**usuario llama a EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) en EAPHost.
-   EAPHost recopila el contexto de la interfaz de usuario mediante una llamada [**a EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) en el método EAP.
-   El método EAP proporciona cualquier información de contexto de interfaz de usuario necesaria en la estructura DE DATOS DE LA INTERFAZ DE USUARIO INTERACTIVA de EAP, donde *dwDataType* se establece en *EapCredExpiryReq* y *pbUiData* apunta a una estructura de tipo [**EAP \_ CRED \_ REQ**](eap-cred-req.md). [**\_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
-   Al rellenar la estructura EAP [**\_ INTERACTIVE UI \_ \_ DATA,**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) este método EAP solo rellenará el parámetro *curCreds* y no establecerá la marca [**EAP UI INPUT FIELD \_ \_ \_ \_ PROPS READ \_ \_ ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) en la estructura **EAP CONFIG INPUT FIELD \_ \_ \_ \_ DATA.**
    > [!Note]  
    > La [**marca EAP UI INPUT FIELD \_ \_ \_ \_ PROPS READ \_ \_ ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) es para los campos de miembro que deben cambiarse.

     

-   Después de recopilar la información de contexto de la interfaz de usuario, el proceso de interfaz de usuario representa una interfaz de usuario para recopilar información de cambio de contraseña del usuario. Esta información se rellena en el parámetro *NewCreds* de la estructura [**EAP \_ CRED \_ EXPIRY \_ REQ.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
-   El proceso de interfaz de usuario pasa la estructura [**\_ \_ RESP**](eap-cred-resp.md) de EAP CRED a EAPHost a través de [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).
-   El proceso de interfaz de usuario pasa este BLOB de usuario al suplicante y el suplicante continúa con las funciones en tiempo de ejecución de EAPHost como de costumbre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escenarios de EAPHost de SSO](why-eaphost-sso.md)
</dt> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




