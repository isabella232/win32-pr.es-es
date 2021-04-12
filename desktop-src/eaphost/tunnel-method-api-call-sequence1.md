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
# <a name="tunnel-method-api-call-sequence"></a><span data-ttu-id="790ff-104">Secuencia de llamadas API de método de túnel</span><span class="sxs-lookup"><span data-stu-id="790ff-104">Tunnel Method API Call Sequence</span></span>

<span data-ttu-id="790ff-105">En este tema se trata la secuencia de llamadas API para los métodos de túnel</span><span class="sxs-lookup"><span data-stu-id="790ff-105">This topic covers the API call sequence for Tunnel Methods</span></span>

## <a name="tunnel-method-call-sequence-overview"></a><span data-ttu-id="790ff-106">Información general sobre la secuencia de llamadas al método de túnel</span><span class="sxs-lookup"><span data-stu-id="790ff-106">Tunnel Method Call Sequence Overview</span></span>

<span data-ttu-id="790ff-107">Cuando el solicitante recibe solicitudes de identidad de usuario y datos de usuario, normalmente se produce el siguiente flujo de llamadas de API.</span><span class="sxs-lookup"><span data-stu-id="790ff-107">When Supplicant gets request for user identity and user data the following API call flow typically occurs.</span></span>

-   <span data-ttu-id="790ff-108">El solicitante llama a EapHostPeerProcessReceivedPacket en EapHost para procesar el paquete recibido del autenticador.</span><span class="sxs-lookup"><span data-stu-id="790ff-108">The Supplicant calls EapHostPeerProcessReceivedPacket on EapHost, to process the packet received from the authenticator.</span></span>
-   <span data-ttu-id="790ff-109">Al procesar este paquete, EAPHost lo determina como paquete IdentityRequest y llama a [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) en el método de túnel para obtener la identidad del usuario que se va a usar para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="790ff-109">Upon processing this packet, EAPHost determines it as IdentityRequest packet and calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on tunnel method to obtain the user identity to use for authentication.</span></span>
-   <span data-ttu-id="790ff-110">Si el método de túnel necesita obtener la identidad del usuario del método interno, llama a [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) en EAPHost interno, que a su vez llama a [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) en el método interno.</span><span class="sxs-lookup"><span data-stu-id="790ff-110">If tunnel method needs to obtain user identity from the inner method, it calls [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) on inner EAPHost, which in turn calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on the inner method.</span></span>

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a><span data-ttu-id="790ff-111">Interacción del usuario con el flujo de llamadas de API de métodos de túnel</span><span class="sxs-lookup"><span data-stu-id="790ff-111">User Interaction with the Tunnel Methods API Call Flow</span></span>

<span data-ttu-id="790ff-112">En algunos casos, cuando la identidad no está disponible o cuando el usuario debe proporcionar información adicional, el método EAP genera un cuadro de diálogo de interfaz de usuario en el suplicante.</span><span class="sxs-lookup"><span data-stu-id="790ff-112">In certain cases, when the identity is not available, or when the user must provide additional information, Eap Method raises an user interface dialog box on the supplicant.</span></span>

<span data-ttu-id="790ff-113">En estos casos, la siguiente secuencia de llamadas tiene lugar normalmente para obtener información directamente del usuario.</span><span class="sxs-lookup"><span data-stu-id="790ff-113">In such cases following call sequence typically takes place to get information directly from the user.</span></span>

-   <span data-ttu-id="790ff-114">El método EAP de túnel devuelve el código de acción para invocar la interfaz de usuario a EapHost.</span><span class="sxs-lookup"><span data-stu-id="790ff-114">Tunnel Eap Method returns action code to invoke UI to EapHost.</span></span> <span data-ttu-id="790ff-115">El solicitante llama a [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)para obtener la información de contexto de la interfaz de usuario actual para el cuadro de diálogo de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="790ff-115">Supplicant calls [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)to obtain the current user interface context information for the user interface dialog box.</span></span>
-   <span data-ttu-id="790ff-116">Después, el suplicante llama a [ **EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span><span class="sxs-lookup"><span data-stu-id="790ff-116">Supplicant then calls [**EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span></span> <span data-ttu-id="790ff-117">Esta función usa la información de contexto de la interfaz de usuario para generar una interfaz de usuario interactiva que se usa para obtener información de credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="790ff-117">This function uses the UI context information to raise an interactive user interface which is used to get credential information from the user.</span></span> <span data-ttu-id="790ff-118">El proceso de la interfaz de usuario carga Eappcfg.dll y obtiene los punteros a EapPeerInvokeInteractiveUI y EapPeerFreeMemory.</span><span class="sxs-lookup"><span data-stu-id="790ff-118">The UI process loads Eappcfg.dll and obtains the pointers to EapPeerInvokeInteractiveUI and EapPeerFreeMemory.</span></span>
    > [!Note]  
    > <span data-ttu-id="790ff-119">Normalmente, el proceso de la interfaz de usuario recopila la interfaz de usuario o controla la interfaz de usuario interactiva y es independiente del proceso del suplicante.</span><span class="sxs-lookup"><span data-stu-id="790ff-119">UI process typically collects UI or handles interactive UI and is separate from the supplicant process.</span></span> <span data-ttu-id="790ff-120">La separación de los dos procesos no es un requisito de EAPHost, pero esto tiene la ventaja de permitir que el proceso de la interfaz de usuario interactúe con el escritorio.</span><span class="sxs-lookup"><span data-stu-id="790ff-120">Separating the two processes is not a requirement of EAPHost, but doing so has the advantage of allowing the UI process to interact with the desktop.</span></span>

     

-   <span data-ttu-id="790ff-121">EapHost llama a [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) en el método de túnel para obtener información de identidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="790ff-121">EapHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on tunnel method to obtain user identity information.</span></span>
-   <span data-ttu-id="790ff-122">Para obtener la identidad del usuario desde el método interno, el método de túnel llama a [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) en EAPHost interno.</span><span class="sxs-lookup"><span data-stu-id="790ff-122">In order to obtain user identity from inner method, tunnel method calls [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) on inner EAPHost.</span></span>
-   <span data-ttu-id="790ff-123">EAPHost interno llama a [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) en el método interno para invocar la interfaz de usuario de identidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="790ff-123">Inner EAPHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on inner method to invoke user identity UI.</span></span>
-   <span data-ttu-id="790ff-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) proporciona información de contexto de la interfaz de usuario nueva o actualizada para el método EAP del mismo nivel cargado en EAPHost después de que se haya generado la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="790ff-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) provides a new or updated UI context information to the EAP peer method loaded on EAPHost after the UI has been raised.</span></span>

<span data-ttu-id="790ff-125">En el diagrama siguiente se explica la secuencia de llamadas API para los métodos de túnel</span><span class="sxs-lookup"><span data-stu-id="790ff-125">Following diagram explains the API Call Sequence for Tunnel Methods</span></span>

![secuencia de llamadas API de métodos de túnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a><span data-ttu-id="790ff-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="790ff-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="790ff-128">Secuencia de llamadas de EAPHost</span><span class="sxs-lookup"><span data-stu-id="790ff-128">EAPHost Call Sequence</span></span>](about-eaphost-call-sequences.md)
</dt> <dt>

[<span data-ttu-id="790ff-129">Secuencia de llamadas API de suplicante</span><span class="sxs-lookup"><span data-stu-id="790ff-129">Supplicant API Call Sequence</span></span>](supplicant-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="790ff-130">Referencia de API suplicante de EAPHost</span><span class="sxs-lookup"><span data-stu-id="790ff-130">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




