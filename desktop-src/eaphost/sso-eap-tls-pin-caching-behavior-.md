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
# <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="cfd63-103">Comportamiento de almacenamiento en caché de PIN EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="cfd63-103">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="cfd63-104">En este tema se proporciona un enfoque paso a paso para resolver las cuestiones de reanudación de la sesión y reautenticación de un usuario móvil en un entorno de SSO EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="cfd63-104">This topic provides a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="cfd63-105">Enfoque paso a paso</span><span class="sxs-lookup"><span data-stu-id="cfd63-105">Step-By-Step Approach</span></span>

<span data-ttu-id="cfd63-106">La lista siguiente representa un enfoque paso a paso para resolver las cuestiones de reanudación de la sesión y reautenticación de un usuario móvil en un entorno de SSO EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="cfd63-106">The following list represents a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

-   <span data-ttu-id="cfd63-107">Después de la primera autenticación correcta en un entorno de SSO con EAP-TLS, el solicitante conserva toda la información relacionada con las credenciales de usuario de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cfd63-107">After the first successful authentication in an SSO environment with EAP-TLS, the supplicant retains all user credential related information by default.</span></span>
    > [!Note]  
    > <span data-ttu-id="cfd63-108">Aunque está sujeto a la implementación del suplicante en particular, es aconsejable que conserve toda la estructura de la [**\_ matriz de \_ \_ campos de entrada de configuración de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) que el suplicante utilizó por última vez en la llamada [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) a EAPHost.</span><span class="sxs-lookup"><span data-stu-id="cfd63-108">Although subject to the particular supplicant implementation, it's advisable for the supplicant to retain the entire [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure that the supplicant last used in the [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) call to EAPHost.</span></span>

     

-   <span data-ttu-id="cfd63-109">A medida que el usuario se desplaza por primera vez y comienza la reautenticación, el solicitante llama de nuevo a [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) con la misma estructura de [**matriz de \_ \_ \_ campos de entrada de configuración de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) ; el solicitante también debe pasar el mismo BLOB de usuario que se conserva después de la primera autenticación correcta.</span><span class="sxs-lookup"><span data-stu-id="cfd63-109">As the user first roams and the re-authentication begins, the supplicant calls [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) again with the same [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure; the supplicant must also pass in the same user BLOB retained after the first successful authentication.</span></span>
-   <span data-ttu-id="cfd63-110">A continuación, EAPHost pasa la información del BLOB de usuario al método EAP.</span><span class="sxs-lookup"><span data-stu-id="cfd63-110">EAPHost then passes the information in the user BLOB to the EAP method.</span></span>
-   <span data-ttu-id="cfd63-111">A su vez, el método EAP actualiza el BLOB de usuario con campos de credenciales (el PIN por ejemplo) proporcionado en *pEapConfigInputFieldArray* y mantiene los valores restantes: el certificado de servidor, por ejemplo, tal como se encontraba en el BLOB de usuario original.</span><span class="sxs-lookup"><span data-stu-id="cfd63-111">The EAP method in turn updates the user BLOB with credential fields - the PIN for example - provided in *pEapConfigInputFieldArray*, and keeps the remaining values - the server certificate for example - as it was in the original user BLOB.</span></span>
-   <span data-ttu-id="cfd63-112">Después de completar estos pasos, el solicitante puede reanudar la autenticación de una manera normal mediante una llamada a la función en tiempo de ejecución [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con este BLOB de usuario.</span><span class="sxs-lookup"><span data-stu-id="cfd63-112">After completing these steps, the supplicant can resume authentication in a normal way by calling the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) run-time function with this user BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfd63-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cfd63-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfd63-114">Escenarios de EAPHost de SSO</span><span class="sxs-lookup"><span data-stu-id="cfd63-114">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="cfd63-115">SSO y PLAP</span><span class="sxs-lookup"><span data-stu-id="cfd63-115">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




