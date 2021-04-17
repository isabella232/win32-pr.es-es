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
# <a name="sso-password-change-behavior"></a><span data-ttu-id="0e47a-103">Comportamiento de cambio de contraseña de SSO</span><span class="sxs-lookup"><span data-stu-id="0e47a-103">SSO Password Change Behavior</span></span>

<span data-ttu-id="0e47a-104">En este tema se proporciona un enfoque paso a paso para resolver el comportamiento del cambio de contraseña de SSO.</span><span class="sxs-lookup"><span data-stu-id="0e47a-104">This topic provides a step-by-step approach for resolving SSO password change behavior.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="0e47a-105">Enfoque paso a paso</span><span class="sxs-lookup"><span data-stu-id="0e47a-105">Step-By-Step Approach</span></span>

<span data-ttu-id="0e47a-106">La lista siguiente representa un enfoque paso a paso para resolver el comportamiento del cambio de contraseña de SSO.</span><span class="sxs-lookup"><span data-stu-id="0e47a-106">The following list represents a step-by-step approach for resolving SSO password change behavior.</span></span>

-   <span data-ttu-id="0e47a-107">Una vez que el método EAP recibe una notificación sobre un cambio de contraseña, el método notifica a EAPHost; A su vez, EAPHost notifica al solicitante devolviendo el código de acción [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="0e47a-107">Once the EAP method is notified about a password change, the method notifies EAPHost; EAPHost in turn notifies the supplicant by returning the action code, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="0e47a-108">Después de recibir el código de acción [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) de EAPHost, el solicitante obtiene el contexto de la interfaz de usuario del método EAP mediante una llamada a la función [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) . A continuación, EAPHost obtiene el contexto de la interfaz de usuario del método EAP mediante una llamada a la función de método correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0e47a-108">After receiving the [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) action code from EAPHost, the supplicant obtains the UI context from the EAP method by calling the [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) function; EAPHost then obtains the UI context from the EAP method by calling the corresponding method function</span></span>
-   <span data-ttu-id="0e47a-109">El suplicante pasa el contexto de la interfaz de usuario al proceso de la interfaz de usuario (mediante algún tipo de comunicación entre procesos).</span><span class="sxs-lookup"><span data-stu-id="0e47a-109">The supplicant passes the UI context to the UI process (using some form of inter-process communication).</span></span>
-   <span data-ttu-id="0e47a-110">El proceso de la interfaz de usuario llama a [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) en EAPHost.</span><span class="sxs-lookup"><span data-stu-id="0e47a-110">The UI process calls [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) on EAPHost.</span></span>
-   <span data-ttu-id="0e47a-111">EAPHost recopila el contexto de la interfaz de usuario mediante una llamada a [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) en el método EAP.</span><span class="sxs-lookup"><span data-stu-id="0e47a-111">EAPHost collects the UI context by calling [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) on the EAP method.</span></span>
-   <span data-ttu-id="0e47a-112">El método EAP proporciona cualquier información de contexto de la interfaz de usuario necesaria en la estructura de [**datos de interfaz de \_ \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , donde *DwDataType* se establece en *EapCredExpiryReq* y *pbUiData* apunta a una estructura de tipo [**\_ \_ req de credenciales de EAP**](eap-cred-req.md).</span><span class="sxs-lookup"><span data-stu-id="0e47a-112">The EAP method provides any necessary UI context information in the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, where *dwDataType* is set to *EapCredExpiryReq* and *pbUiData* points to a structure of type [**EAP\_CRED\_REQ**](eap-cred-req.md).</span></span>
-   <span data-ttu-id="0e47a-113">Al rellenar la estructura de datos de la [**\_ interfaz de \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , este método EAP solo rellenará el parámetro *curCreds* y no establecerá la marca de [**\_ \_ \_ \_ \_ \_ solo lectura del campo de entrada de la interfaz de usuario EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) en la estructura de **\_ \_ \_ \_ datos del campo de entrada de configuración de EAP** .</span><span class="sxs-lookup"><span data-stu-id="0e47a-113">While populating the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, this EAP method will only fill in the *curCreds* parameter, and not set the [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag in the **EAP\_CONFIG\_INPUT\_FIELD\_DATA** structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="0e47a-114">La marca de [**\_ \_ \_ \_ \_ \_ solo lectura del campo de entrada**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) de la interfaz de usuario de EAP es para los campos de miembro que deben cambiarse.</span><span class="sxs-lookup"><span data-stu-id="0e47a-114">The [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag is for member field(s) which need to be changed.</span></span>

     

-   <span data-ttu-id="0e47a-115">Tras recopilar el contexto de la interfaz de usuario informtion, el proceso de IU representa una interfaz de usuario para recopilar información de cambio de contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="0e47a-115">Having collected the UI context informtion, the UI process renders a UI to collect change password information from the user.</span></span> <span data-ttu-id="0e47a-116">Esta información se rellena en el parámetro *NewCreds* de la estructura del [**\_ \_ \_ req de expiración**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) de la credencial de EAP.</span><span class="sxs-lookup"><span data-stu-id="0e47a-116">This information is populated in the *NewCreds* parameter of the [**EAP\_CRED\_EXPIRY\_REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) structure.</span></span>
-   <span data-ttu-id="0e47a-117">El proceso de la interfaz de usuario vuelve a pasar la estructura de [**\_ \_ resp de EAP**](eap-cred-resp.md) a EAPHost a través de [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span><span class="sxs-lookup"><span data-stu-id="0e47a-117">The UI process passes the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure back to EAPHost via [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span></span>
-   <span data-ttu-id="0e47a-118">El proceso de IU pasa este BLOB de usuario al suplicante y el suplicante continúa con las funciones de tiempo de ejecución de EAPHost como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="0e47a-118">The UI process passes this user BLOB to the supplicant, and the supplicant continues with EAPHost run-time functions as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e47a-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e47a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e47a-120">Escenarios de EAPHost de SSO</span><span class="sxs-lookup"><span data-stu-id="0e47a-120">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="0e47a-121">SSO y PLAP</span><span class="sxs-lookup"><span data-stu-id="0e47a-121">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




