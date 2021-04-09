---
title: Comportamiento de almacenamiento en caché de PIN EAP-TLS
description: Proporciona un enfoque paso a paso para resolver las cuestiones relacionadas con la reanudación de la sesión y la reautenticación de un usuario móvil en un entorno EAP-TLS de SSO.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7c4e3058598f98327570fbcd0347cfb84e5825
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104149013"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a>Comportamiento de almacenamiento en caché de PIN EAP-TLS

En este tema se proporciona un enfoque paso a paso para resolver las cuestiones de reanudación de la sesión y reautenticación de un usuario móvil en un entorno de SSO EAP-TLS.

## <a name="step-by-step-approach"></a>Enfoque paso a paso

La lista siguiente representa un enfoque paso a paso para resolver las cuestiones de reanudación de la sesión y reautenticación de un usuario móvil en un entorno de SSO EAP-TLS.

-   Después de la primera autenticación correcta en un entorno de SSO con EAP-TLS, el solicitante conserva toda la información relacionada con las credenciales de usuario de forma predeterminada.
    > [!Note]  
    > Aunque está sujeto a la implementación del suplicante en particular, es aconsejable que conserve toda la estructura de la [**\_ matriz de \_ \_ campos de entrada de configuración de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) que el suplicante utilizó por última vez en la llamada [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) a EAPHost.

     

-   A medida que el usuario se desplaza por primera vez y comienza la reautenticación, el solicitante llama de nuevo a [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) con la misma estructura de [**matriz de \_ \_ \_ campos de entrada de configuración de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) ; el solicitante también debe pasar el mismo BLOB de usuario que se conserva después de la primera autenticación correcta.
-   A continuación, EAPHost pasa la información del BLOB de usuario al método EAP.
-   A su vez, el método EAP actualiza el BLOB de usuario con campos de credenciales (el PIN por ejemplo) proporcionado en *pEapConfigInputFieldArray* y mantiene los valores restantes: el certificado de servidor, por ejemplo, tal como se encontraba en el BLOB de usuario original.
-   Después de completar estos pasos, el solicitante puede reanudar la autenticación de una manera normal mediante una llamada a la función en tiempo de ejecución [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con este BLOB de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escenarios de EAPHost de SSO](why-eaphost-sso.md)
</dt> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




