---
title: Implementación de la compatibilidad de NAP con métodos EAP
description: Obtenga información sobre cómo implementar la compatibilidad de NAP para un suplicante de EAPHost. Vea los temas NAP relacionados con EAPHost y ver recursos adicionales disponibles.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104078641"
---
# <a name="implementing-nap-support-for-eap-methods"></a><span data-ttu-id="c6015-104">Implementación de la compatibilidad de NAP con métodos EAP</span><span class="sxs-lookup"><span data-stu-id="c6015-104">Implementing NAP Support for EAP Methods</span></span>

<span data-ttu-id="c6015-105">En este tema se explica cómo implementar NAP para un suplicante de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="c6015-105">This topic explains how to implement NAP for an EAPHost supplicant.</span></span> <span data-ttu-id="c6015-106">En Windows Vista y Windows Server 2008, hay un cliente de cumplimiento NAP (NAP EC) disponible para las conexiones autenticadas de [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="c6015-106">In Windows Vista and Windows Server 2008 a NAP Enforcement Client (NAP EC) is available for [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authenticated connections.</span></span>

## <a name="implementing-network-access-protection-nap"></a><span data-ttu-id="c6015-107">Implementación de protección de acceso a redes (NAP)</span><span class="sxs-lookup"><span data-stu-id="c6015-107">Implementing Network Access Protection (NAP)</span></span>

<span data-ttu-id="c6015-108">Para admitir NAP, un suplicante de EAPHost implementa una función de devolución de llamada que coincide con el prototipo de devolución de llamada [**NotificationHandler**](/previous-versions/windows/desktop/api) y debe proporcionar un puntero a esta función de devolución de llamada al llamar a [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="c6015-108">To support NAP, an EAPHost supplicant implements a callback function matching the [**NotificationHandler**](/previous-versions/windows/desktop/api) callback prototype and must provide a pointer to this callback function when calling [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>

<span data-ttu-id="c6015-109">La función de devolución de llamada toma dos parámetros.</span><span class="sxs-lookup"><span data-stu-id="c6015-109">The callback function takes two parameters.</span></span>

-   <span data-ttu-id="c6015-110">GUID que identifica de forma única la interfaz asociada a la autenticación.</span><span class="sxs-lookup"><span data-stu-id="c6015-110">A GUID that uniquely identifies the interface associated with the authentication.</span></span>
-   <span data-ttu-id="c6015-111">Puntero VOID a una estructura de datos opaca suministrada por el solicitante.</span><span class="sxs-lookup"><span data-stu-id="c6015-111">A VOID pointer to an opaque data structure that is supplied by the supplicant.</span></span>

<span data-ttu-id="c6015-112">EAPHost llamará a la función de devolución de llamada proporcionada por el suplicante con el GUID de la interfaz única y el puntero VOID cuando cambie el estado de cuarentena del equipo.</span><span class="sxs-lookup"><span data-stu-id="c6015-112">EAPHost will call the supplicant-provided callback function with the unique interface GUID and the VOID pointer when the quarantine state of the machine changes.</span></span> <span data-ttu-id="c6015-113">Cuando EAPHost llama a la función de devolución de llamada proporcionada por el suplicante, el suplicante responde cerrando la conexión de red lógica identificada por el puntero de interfaz GUID/VOID y comienza de nuevo la autenticación mediante **EapHostPeerBeginSession**.</span><span class="sxs-lookup"><span data-stu-id="c6015-113">When EAPHost calls the supplicant-provided callback function, the supplicant responds by tearing down the logical network connection identified by the interface GUID/VOID pointer and begins authentication again using **EapHostPeerBeginSession**.</span></span>

<span data-ttu-id="c6015-114">EAPHost puede llamar a la función de devolución de llamada proporcionada por el suplicante en cualquier momento: antes, durante una autenticación activa o después de que se haya completado la autenticación (después de que se haya llamado a [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) pero no antes de que se haya llamado a [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ).</span><span class="sxs-lookup"><span data-stu-id="c6015-114">EAPHost may call the supplicant-supplied callback function at any time: before, during an active authentication, or after the authentication has been completed (after [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) has been called but not before [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) has been called).</span></span> <span data-ttu-id="c6015-115">El suplicante siempre debe responder si se anula la conexión de red lógica y se vuelve a autenticar.</span><span class="sxs-lookup"><span data-stu-id="c6015-115">The supplicant should always respond by tearing down the logical network connection and re-authenticating.</span></span>

<span data-ttu-id="c6015-116">Si el solicitante se está cerrando o está eligiendo dejar de recibir una notificación de cambios de estado de aislamiento, el solicitante debe llamar a [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) y especificar el GUID de interfaz adecuado.</span><span class="sxs-lookup"><span data-stu-id="c6015-116">If the supplicant is shutting down or choosing to no longer receive notification of isolation state changes, the supplicant should call [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) and specify the appropriate interface GUID.</span></span> <span data-ttu-id="c6015-117">Si el solicitante desea determinar el aislamiento de la conexión de red lógica, el solicitante puede obtener esa información de **EapHostPeerMethodResult. isolationState** cuando [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) se obtiene de [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span><span class="sxs-lookup"><span data-stu-id="c6015-117">If the supplicant wishes to determine the isolation of the logical network connection, the supplicant can obtain that information from **EapHostPeerMethodResult.isolationState** when the [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) is obtained from [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span></span>

## <a name="eaphost-related-nap-information"></a><span data-ttu-id="c6015-118">Información de NAP relacionada con EAPHost</span><span class="sxs-lookup"><span data-stu-id="c6015-118">EAPHost Related NAP Information</span></span>

<span data-ttu-id="c6015-119">Para información sobre NAP relacionada con la API de EAPHost, consulte los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="c6015-119">For EAPHost API related NAP information refer to the following topics.</span></span>

-   [<span data-ttu-id="c6015-120">**\_tipo de atributo EAP \_**</span><span class="sxs-lookup"><span data-stu-id="c6015-120">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [<span data-ttu-id="c6015-121">**ERROR de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="c6015-121">**EAP\_ERROR**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [<span data-ttu-id="c6015-122">Preguntas más frecuentes sobre el suplicante de EAPHost</span><span class="sxs-lookup"><span data-stu-id="c6015-122">EAPHost Supplicant Frequently Asked Questions</span></span>](eaphost-supplicant-frequently-asked-questions.md)
-   [<span data-ttu-id="c6015-123">**Propiedades del método EAP**</span><span class="sxs-lookup"><span data-stu-id="c6015-123">**EAP Method Properties**</span></span>](eap-method-properties.md)
-   [<span data-ttu-id="c6015-124">**EapHostPeerBeginSession**</span><span class="sxs-lookup"><span data-stu-id="c6015-124">**EapHostPeerBeginSession**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [<span data-ttu-id="c6015-125">**Constantes de información y errores relacionados con EAP**</span><span class="sxs-lookup"><span data-stu-id="c6015-125">**EAP Related Error and Information Constants**</span></span>](eap-related-error-and-information-constants.md)
-   [<span data-ttu-id="c6015-126">**Estado de aislamiento \_**</span><span class="sxs-lookup"><span data-stu-id="c6015-126">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [<span data-ttu-id="c6015-127">**NotificationHandler**</span><span class="sxs-lookup"><span data-stu-id="c6015-127">**NotificationHandler**</span></span>](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a><span data-ttu-id="c6015-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c6015-128">Additional Resources</span></span>


-   <span data-ttu-id="c6015-129">Para obtener una lista de recursos de NAP, consulte [protección de acceso a redes](https://go.microsoft.com/fwlink/p/?linkid=84107).</span><span class="sxs-lookup"><span data-stu-id="c6015-129">For a list of NAP resources, see [Network Access Protection](https://go.microsoft.com/fwlink/p/?linkid=84107).</span></span>
-   <span data-ttu-id="c6015-130">Para obtener información sobre el informe de mantenimiento, consulte [mensajes de informe de mantenimiento (SOH) de protección de acceso a redes (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83918).</span><span class="sxs-lookup"><span data-stu-id="c6015-130">For Statement of Health information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>
-   <span data-ttu-id="c6015-131">Para la página web del grupo de redes empresariales y el blog, consulte [protección de acceso a redes (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span><span class="sxs-lookup"><span data-stu-id="c6015-131">For the Enterprise Networking Group webpage and blog, see [Network Access Protection (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span></span>
-   <span data-ttu-id="c6015-132">Para obtener información sobre la API de NAP, consulte [protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page).</span><span class="sxs-lookup"><span data-stu-id="c6015-132">For NAP API information, see [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page).</span></span>


## <a name="related-topics"></a><span data-ttu-id="c6015-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6015-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6015-134">Configuración de la interfaz de usuario del método EAP</span><span class="sxs-lookup"><span data-stu-id="c6015-134">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="c6015-135">Habilitar directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="c6015-135">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="c6015-136">Implementación de la compatibilidad de In-Band NAP con métodos EAP</span><span class="sxs-lookup"><span data-stu-id="c6015-136">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="c6015-137">Transferencia de datos entre el suplicante y los métodos EAP</span><span class="sxs-lookup"><span data-stu-id="c6015-137">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="c6015-138">Suplicantes de EAPHost</span><span class="sxs-lookup"><span data-stu-id="c6015-138">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 