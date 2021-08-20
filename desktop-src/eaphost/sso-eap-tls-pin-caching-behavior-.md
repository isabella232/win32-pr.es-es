---
title: Comportamiento del almacenamiento en caché de PIN EAP-TLS de SSO
description: Proporciona un enfoque paso a paso para resolver los problemas de reanudación de sesión y re autenticación de un usuario móvil en un entorno EAP-TLS de SSO.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bc8cb112a6def55085cbd0b94068407320e4116a4b0161d7d923319257258f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085889"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a>Comportamiento del almacenamiento en caché de PIN EAP-TLS de SSO

En este tema se proporciona un enfoque paso a paso para resolver cuestiones relacionadas con la reanudación de la sesión y la re autenticación de un usuario móvil en un entorno EAP-TLS de SSO.

## <a name="step-by-step-approach"></a>Enfoque paso a paso

En la lista siguiente se representa un enfoque paso a paso para resolver los problemas de reanudación de sesión y re autenticación de un usuario móvil en un entorno EAP-TLS de SSO.

-   Después de la primera autenticación correcta en un entorno de SSO con EAP-TLS, el suplicante conserva toda la información relacionada con las credenciales de usuario de forma predeterminada.
    > [!Note]  
    > Aunque está sujeto a la implementación de suplicante determinada, es aconsejable que el suplicante conserve toda la estructura DE LA MATRIZ DE CAMPO DE ENTRADA DE CONFIGURACIÓN DE EAP que el suplicante usó por última vez en la llamada [**eapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) a EAPHost. [**\_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)

     

-   A medida que el usuario se desmorona por primera vez y comienza la nueva autenticación, el suplicante llama de nuevo a [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) con la misma estructura [**EAP CONFIG INPUT FIELD \_ \_ \_ ARRAY;**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) el suplicante también debe pasar el mismo BLOB de usuario retenido después de la primera autenticación correcta.
-   A continuación, EAPHost pasa la información del blob de usuario al método EAP.
-   A su vez, el método EAP actualiza el blob de usuario con campos de credencial (por ejemplo, el PIN) proporcionado en *pEapConfigInputFieldArray* y mantiene los valores restantes (el certificado de servidor, por ejemplo), tal como estaba en el blob de usuario original.
-   Después de completar estos pasos, el suplicante puede reanudar la autenticación de forma normal llamando a la función en tiempo de ejecución [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con este BLOB de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escenarios de EAPHost de SSO](why-eaphost-sso.md)
</dt> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




