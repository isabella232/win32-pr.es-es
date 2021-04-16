---
title: Marcas de método EAP (Eaptypes. h)
description: Las marcas de método EAP se utilizan en las funciones suplicante, autenticador y del mismo nivel para especificar los comportamientos de una sesión de autenticación EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488914"
---
# <a name="eap-method-flags"></a><span data-ttu-id="cd82b-103">Marcas de método EAP</span><span class="sxs-lookup"><span data-stu-id="cd82b-103">EAP Method Flags</span></span>

<span data-ttu-id="cd82b-104">Las marcas de método EAP se utilizan en las funciones suplicante, autenticador y del mismo nivel para especificar los comportamientos de una sesión de autenticación EAP.</span><span class="sxs-lookup"><span data-stu-id="cd82b-104">The EAP method flags are used within the supplicant, authenticator, and peer functions to specify behaviors of an EAP authentication session.</span></span>

<dl> <dt>

<span data-ttu-id="cd82b-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Marca EAP \_ Reserved1**</span><span class="sxs-lookup"><span data-stu-id="cd82b-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP\_FLAG\_Reserved1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cd82b-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-107">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cd82b-107">Do not use.</span></span> <span data-ttu-id="cd82b-108">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cd82b-108">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**\_marca EAP \_ no \_ interactiva**</span><span class="sxs-lookup"><span data-stu-id="cd82b-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP\_FLAG\_NON\_INTERACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cd82b-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-111">No mostrar una interfaz de usuario (UI).</span><span class="sxs-lookup"><span data-stu-id="cd82b-111">Do not display a user interface (UI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**Inicio de sesión de \_ marca EAP \_**</span><span class="sxs-lookup"><span data-stu-id="cd82b-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP\_FLAG\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-113">0x00000004</span><span class="sxs-lookup"><span data-stu-id="cd82b-113">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-114">Los datos de usuario se obtuvieron del inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="cd82b-114">User data was obtained from Windows logon.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**\_ \_ vista previa de la marca EAP**</span><span class="sxs-lookup"><span data-stu-id="cd82b-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP\_FLAG\_PREVIEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-116">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cd82b-116">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-117">Mostrar la interfaz de usuario de credenciales antes de la autenticación, incluso si las credenciales almacenadas en caché están presentes.</span><span class="sxs-lookup"><span data-stu-id="cd82b-117">Show credentials UI before authenticating, even if cached credentials are present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ de MARCA \_ Reserved2**</span><span class="sxs-lookup"><span data-stu-id="cd82b-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span> **EAP\_FLAG\_Reserved2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd82b-119">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-120">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cd82b-120">Do not use.</span></span> <span data-ttu-id="cd82b-121">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cd82b-121">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**\_autenticación de \_ equipo de marca EAP \_**</span><span class="sxs-lookup"><span data-stu-id="cd82b-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP\_FLAG\_MACHINE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-123">0x00000020</span><span class="sxs-lookup"><span data-stu-id="cd82b-123">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-124">Usar autenticación a nivel de equipo; Si no se establece esta marca, indica que se está usando la autenticación de nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="cd82b-124">Use machine level authentication; not setting this flag indicates user level authentication is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**\_acceso de \_ invitado de marca EAP \_**</span><span class="sxs-lookup"><span data-stu-id="cd82b-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP\_FLAG\_GUEST\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="cd82b-126">0x00000040</span><span class="sxs-lookup"><span data-stu-id="cd82b-126">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-127">Indica una solicitud para proporcionar acceso de invitado.</span><span class="sxs-lookup"><span data-stu-id="cd82b-127">Indicates a request to provide guest access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Marca EAP \_ Reserved3**</span><span class="sxs-lookup"><span data-stu-id="cd82b-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP\_FLAG\_Reserved3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-129">0x00000080</span><span class="sxs-lookup"><span data-stu-id="cd82b-129">0x00000080</span></span> 
</dt> <dt>



<span data-ttu-id="cd82b-130">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cd82b-130">Do not use.</span></span> <span data-ttu-id="cd82b-131">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cd82b-131">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ de MARCA \_ Reserved4**</span><span class="sxs-lookup"><span data-stu-id="cd82b-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span> **EAP\_FLAG\_Reserved4**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-133">0x00000100</span><span class="sxs-lookup"><span data-stu-id="cd82b-133">0x00000100</span></span> 
</dt> <dt>



<span data-ttu-id="cd82b-134">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cd82b-134">Do not use.</span></span> <span data-ttu-id="cd82b-135">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cd82b-135">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**\_marca EAP \_ reanudar \_ desde \_ hibernación**</span><span class="sxs-lookup"><span data-stu-id="cd82b-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP\_FLAG\_RESUME\_FROM\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-137">0x00000200</span><span class="sxs-lookup"><span data-stu-id="cd82b-137">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-138">Indica que se trata de la primera llamada después de que la actividad del equipo se haya reanudado desde un período de hibernación.</span><span class="sxs-lookup"><span data-stu-id="cd82b-138">Indicates this is the first call after machine activity has resumed from a period of hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ de MARCA \_ Reserved5**</span><span class="sxs-lookup"><span data-stu-id="cd82b-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span> **EAP\_FLAG\_Reserved5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-140">0x00000400</span><span class="sxs-lookup"><span data-stu-id="cd82b-140">0x00000400</span></span> 
</dt> <dt>



<span data-ttu-id="cd82b-141">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cd82b-141">Do not use.</span></span> <span data-ttu-id="cd82b-142">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cd82b-142">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Marca EAP \_ Reserved6**</span><span class="sxs-lookup"><span data-stu-id="cd82b-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP\_FLAG\_Reserved6**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-144">0x00000800</span><span class="sxs-lookup"><span data-stu-id="cd82b-144">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-145">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cd82b-145">Do not use.</span></span> <span data-ttu-id="cd82b-146">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cd82b-146">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_ \_ autenticación completa de la marca EAP \_**</span><span class="sxs-lookup"><span data-stu-id="cd82b-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP\_FLAG\_FULL\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-148">0x00001000</span><span class="sxs-lookup"><span data-stu-id="cd82b-148">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-149">Indica que los métodos de túnel deben realizar una autenticación completa en lugar de una versión abreviada, como la [reconexión rápida de EAP protegido (PEAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="cd82b-149">Indicates that tunnel methods should perform a full authentication instead of an abbreviated version, such as [Protected EAP (PEAP) Fast Reconnect](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**marca de EAP \_ \_ preferida de \_ \_ credenciales Alt**</span><span class="sxs-lookup"><span data-stu-id="cd82b-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP\_FLAG\_PREFER\_ALT\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="cd82b-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-152">Indica que las credenciales que se pasan a [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) son preferibles a todas las demás formas de recuperación de credenciales, incluso si los datos de configuración pasados a la función actual solicitan un modo diferente de recuperación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="cd82b-152">Indicates credentials passed into [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) are preferred to all other forms of credential retrieval, even if configuration data passed into the current function requests a different mode of credential retrieval.</span></span>

> [!Note]  
> <span data-ttu-id="cd82b-153">Esta marca solo se usa en [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="cd82b-153">This flag is only used by [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Marca EAP \_ Reserved7**</span><span class="sxs-lookup"><span data-stu-id="cd82b-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP\_FLAG\_Reserved7**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-155">0x00004000</span><span class="sxs-lookup"><span data-stu-id="cd82b-155">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-156">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cd82b-156">Do not use.</span></span> <span data-ttu-id="cd82b-157">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cd82b-157">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**cambio de estado de mantenimiento de marca de EAP \_ del mismo nivel \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd82b-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**EAP\_PEER\_FLAG\_HEALTH\_STATE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-159">0x00008000</span><span class="sxs-lookup"><span data-stu-id="cd82b-159">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-160">Indica que la causa de la reautenticación es una devolución de llamada de [protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP); NAP inició la sesión de autenticación porque cambió el estado de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="cd82b-160">Indicates the cause of re-authentication is a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) callback; NAP initiated the authentication session because the health state changed.</span></span> <span data-ttu-id="cd82b-161">Esta marca solo se debe enviar cuando se llama a esta función mediante una devolución de llamada de [*NotificationHandler*](/previous-versions/windows/desktop/api) específica de NAP proporcionada por una llamada anterior a esta función.</span><span class="sxs-lookup"><span data-stu-id="cd82b-161">This flag must be sent only when this function is called by a NAP-specific [*NotificationHandler*](/previous-versions/windows/desktop/api) callback provided by a previous call to this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_marca EAP \_ suprimir \_ UI**</span><span class="sxs-lookup"><span data-stu-id="cd82b-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP\_FLAG\_SUPRESS\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-163">0x00010000</span><span class="sxs-lookup"><span data-stu-id="cd82b-163">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-164">Continúe la autenticación con la información disponible.</span><span class="sxs-lookup"><span data-stu-id="cd82b-164">Continue authentication with available information.</span></span> <span data-ttu-id="cd82b-165">Si la autenticación no puede continuar, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="cd82b-165">If the authentication cannot proceed then fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_Inicio de \_ sesión previo de marca EAP \_**</span><span class="sxs-lookup"><span data-stu-id="cd82b-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP\_FLAG\_PRE\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-167">0x00020000</span><span class="sxs-lookup"><span data-stu-id="cd82b-167">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-168">Indica que EAPHost debe proporcionar el inicio de sesión único (SSO).</span><span class="sxs-lookup"><span data-stu-id="cd82b-168">Indicates that EAPHost should provide Single-Sign-On (SSO).</span></span> <span data-ttu-id="cd82b-169">Para obtener más información, consulte [SSO y PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="cd82b-169">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**\_autenticación de \_ usuario de marca EAP \_**</span><span class="sxs-lookup"><span data-stu-id="cd82b-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP\_FLAG\_USER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-171">0x00040000</span><span class="sxs-lookup"><span data-stu-id="cd82b-171">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-172">Indica la autenticación de nivel de usuario para métodos heredados que no pueden establecer la autenticación del **\_ equipo de marca \_ \_ EAP**.</span><span class="sxs-lookup"><span data-stu-id="cd82b-172">Indicates user level authentication for legacy methods that cannot set **EAP\_FLAG\_MACHINE\_AUTH**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_marca EAP \_ de \_ solo lectura**</span><span class="sxs-lookup"><span data-stu-id="cd82b-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP\_FLAG\_CONFG\_READONLY**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="cd82b-174">0x00080000</span><span class="sxs-lookup"><span data-stu-id="cd82b-174">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-175">Indica que la configuración se puede ver pero no actualizar.</span><span class="sxs-lookup"><span data-stu-id="cd82b-175">Indicates the configuration can be viewed but not updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd82b-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Marca EAP \_ Reserved8**</span><span class="sxs-lookup"><span data-stu-id="cd82b-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP\_FLAG\_Reserved8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd82b-177">0x00100000</span><span class="sxs-lookup"><span data-stu-id="cd82b-177">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="cd82b-178">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cd82b-178">Do not use.</span></span> <span data-ttu-id="cd82b-179">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cd82b-179">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd82b-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd82b-180">Requirements</span></span>



| <span data-ttu-id="cd82b-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd82b-181">Requirement</span></span> | <span data-ttu-id="cd82b-182">Value</span><span class="sxs-lookup"><span data-stu-id="cd82b-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd82b-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd82b-183">Minimum supported client</span></span><br/> | <span data-ttu-id="cd82b-184">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cd82b-184">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd82b-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd82b-185">Minimum supported server</span></span><br/> | <span data-ttu-id="cd82b-186">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd82b-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd82b-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd82b-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd82b-188"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd82b-188"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd82b-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd82b-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd82b-190">Constantes de EAPHost comunes</span><span class="sxs-lookup"><span data-stu-id="cd82b-190">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

