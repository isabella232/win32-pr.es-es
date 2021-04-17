---
description: Contiene información sobre el perfil de conexión de 802.1 X que se usa actualmente para la autenticación de 802.1 X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: Estructura de ONEX_CONNECTION_PROFILE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687433"
---
# <a name="onex_connection_profile-structure"></a><span data-ttu-id="3306b-103">Estructura de Perfil de \_ conexión Onex \_</span><span class="sxs-lookup"><span data-stu-id="3306b-103">ONEX\_CONNECTION\_PROFILE structure</span></span>

<span data-ttu-id="3306b-104">La estructura de **\_ \_ Perfil de conexión Onex** contiene información sobre el perfil de conexión de 802.1 x que se usa actualmente para la autenticación de 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-104">The **ONEX\_CONNECTION\_PROFILE** structure contains information on the 802.1X connection profile currently used for 802.1X authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="3306b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3306b-105">Syntax</span></span>


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a><span data-ttu-id="3306b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3306b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3306b-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="3306b-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-108">La versión de esta estructura de **\_ \_ Perfil de conexión Onex** .</span><span class="sxs-lookup"><span data-stu-id="3306b-108">The version of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-109">**dwTotalLen**</span><span class="sxs-lookup"><span data-stu-id="3306b-109">**dwTotalLen**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-110">Longitud, en bytes, de esta estructura **de \_ \_ Perfil de conexión Onex** .</span><span class="sxs-lookup"><span data-stu-id="3306b-110">The length, in bytes, of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-111">**fOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="3306b-111">**fOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-112">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwOneXSupplicantFlags** .</span><span class="sxs-lookup"><span data-stu-id="3306b-112">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwOneXSupplicantFlags** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-113">**fsupplicantMode**</span><span class="sxs-lookup"><span data-stu-id="3306b-113">**fsupplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-114">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **supplicantMode** .</span><span class="sxs-lookup"><span data-stu-id="3306b-114">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **supplicantMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-115">**fauthMode**</span><span class="sxs-lookup"><span data-stu-id="3306b-115">**fauthMode**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-116">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **authMode** .</span><span class="sxs-lookup"><span data-stu-id="3306b-116">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **authMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-117">**fHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="3306b-117">**fHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-118">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwHeldPeriod** .</span><span class="sxs-lookup"><span data-stu-id="3306b-118">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwHeldPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-119">**fAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="3306b-119">**fAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-120">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwAuthPeriod** .</span><span class="sxs-lookup"><span data-stu-id="3306b-120">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwAuthPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-121">**fStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="3306b-121">**fStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-122">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwStartPeriod** .</span><span class="sxs-lookup"><span data-stu-id="3306b-122">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwStartPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-123">**fMaxStart**</span><span class="sxs-lookup"><span data-stu-id="3306b-123">**fMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-124">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwMaxStart** .</span><span class="sxs-lookup"><span data-stu-id="3306b-124">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxStart** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-125">**fMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="3306b-125">**fMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-126">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwMaxAuthFailures** .</span><span class="sxs-lookup"><span data-stu-id="3306b-126">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxAuthFailures** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-127">**fNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="3306b-127">**fNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-128">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwNetworkAuthTimeout** .</span><span class="sxs-lookup"><span data-stu-id="3306b-128">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthTimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-129">**fAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="3306b-129">**fAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-130">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **bAllowLogonDialogs** .</span><span class="sxs-lookup"><span data-stu-id="3306b-130">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bAllowLogonDialogs** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-131">**fNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="3306b-131">**fNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-132">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwNetworkAuthWithUITimeout** .</span><span class="sxs-lookup"><span data-stu-id="3306b-132">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthWithUITimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-133">**fUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="3306b-133">**fUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-134">Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **bUserBasedVLan** .</span><span class="sxs-lookup"><span data-stu-id="3306b-134">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bUserBasedVLan** member.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-135">**dwOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="3306b-135">**dwOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-136">Un conjunto de marcas 802.1 X que pueden estar presentes en el perfil.</span><span class="sxs-lookup"><span data-stu-id="3306b-136">A set of 802.1X flags that can be present in the profile.</span></span> <span data-ttu-id="3306b-137">Estas marcas están reservadas para uso interno por parte del módulo de autenticación 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="3306b-137">These flags are reserved for internal use by the 802.1X authentication module.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-138">**supplicantMode**</span><span class="sxs-lookup"><span data-stu-id="3306b-138">**supplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-139">El elemento supplicantMode en el esquema 802.1 X que especifica el método de transmisión utilizado para los mensajes de EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="3306b-139">The supplicantMode element in the 802.1X schema that specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="3306b-140">Para obtener más información, vea el [**elemento supplicantMode (Onex)**](onexschema-supplicantmode-onex-element.md) en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-140">For more information, see the [**supplicantMode (OneX) Element**](onexschema-supplicantmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="3306b-141">Value</span><span class="sxs-lookup"><span data-stu-id="3306b-141">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="3306b-142">Significado</span><span class="sxs-lookup"><span data-stu-id="3306b-142">Meaning</span></span>                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <span data-ttu-id="3306b-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3306b-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3306b-144">No se transmiten los mensajes de EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="3306b-144">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="3306b-145">Válido solo para perfiles de LAN con cable.</span><span class="sxs-lookup"><span data-stu-id="3306b-145">Valid for wired LAN profiles only.</span></span><br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <span data-ttu-id="3306b-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3306b-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="3306b-147">El cliente determina cuándo se deben enviar los paquetes de EAPOL-Start en función de la capacidad de la red.</span><span class="sxs-lookup"><span data-stu-id="3306b-147">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="3306b-148">EAPOL-Start mensajes solo se envían cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="3306b-148">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="3306b-149">Válido solo para perfiles de LAN con cable.</span><span class="sxs-lookup"><span data-stu-id="3306b-149">Valid for wired LAN profiles only.</span></span><br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <span data-ttu-id="3306b-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3306b-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="3306b-151">EAPOL-Start mensajes se transmiten según lo especificado por 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="3306b-151">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="3306b-152">Válido para perfiles de LAN inalámbrica y cableada.</span><span class="sxs-lookup"><span data-stu-id="3306b-152">Valid for both wired and wireless LAN profiles.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="3306b-153">**authMode**</span><span class="sxs-lookup"><span data-stu-id="3306b-153">**authMode**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-154">El elemento authMode en el esquema 802.1 X que especifica el tipo de credenciales usado para la autenticación 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="3306b-154">The authMode element in the 802.1X schema that specifies the type of credentials used for 802.1X authentication.</span></span> <span data-ttu-id="3306b-155">Para obtener más información, vea el [**elemento authMode (Onex)**](onexschema-authmode-onex-element.md) en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-155">For more information, see the [**authMode (OneX) Element**](onexschema-authmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="3306b-156">Value</span><span class="sxs-lookup"><span data-stu-id="3306b-156">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="3306b-157">Significado</span><span class="sxs-lookup"><span data-stu-id="3306b-157">Meaning</span></span>                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <span data-ttu-id="3306b-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3306b-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3306b-159">Usar credenciales de equipo o de usuario.</span><span class="sxs-lookup"><span data-stu-id="3306b-159">Use machine or user credentials.</span></span> <span data-ttu-id="3306b-160">Cuando un usuario ha iniciado sesión, se usan las credenciales del usuario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="3306b-160">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="3306b-161">Cuando ningún usuario ha iniciado sesión, se usan las credenciales del equipo.</span><span class="sxs-lookup"><span data-stu-id="3306b-161">When no user is logged on, machine credentials are used.</span></span><br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <span data-ttu-id="3306b-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3306b-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="3306b-163">Usar solo credenciales de equipo.</span><span class="sxs-lookup"><span data-stu-id="3306b-163">Use machine credentials only.</span></span><br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <span data-ttu-id="3306b-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3306b-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="3306b-165">Usar solo credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="3306b-165">Use user credentials only.</span></span><br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <span data-ttu-id="3306b-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3306b-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span></span> </dl>                                 | <span data-ttu-id="3306b-167">Usar solo credenciales de invitado (vacío).</span><span class="sxs-lookup"><span data-stu-id="3306b-167">Use guest (empty) credentials only.</span></span><br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <span data-ttu-id="3306b-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3306b-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="3306b-169">No se especifican las credenciales que se van a usar.</span><span class="sxs-lookup"><span data-stu-id="3306b-169">Credentials to use are not specified.</span></span><br/>                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="3306b-170">**dwHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="3306b-170">**dwHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-171">El elemento heldPeriod en el esquema 802.1 X que especifica el período de tiempo, en segundos, en el que un cliente no volverá a intentar la autenticación después de un intento de autenticación erróneo.</span><span class="sxs-lookup"><span data-stu-id="3306b-171">The heldPeriod element in the 802.1X schema that specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span> <span data-ttu-id="3306b-172">Para obtener más información, vea el [**elemento heldPeriod (Onex)**](onexschema-heldperiod-onex-element.md) en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-172">For more information, see the [**heldPeriod (OneX) Element**](onexschema-heldperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-173">**dwAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="3306b-173">**dwAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-174">El elemento authPeriod en el esquema 802.1 X que especifica el período de tiempo máximo, en segundos, en el que un cliente espera una respuesta del autenticador.</span><span class="sxs-lookup"><span data-stu-id="3306b-174">The authPeriod element in the 802.1X schema that specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="3306b-175">Si no se recibe una respuesta dentro del período especificado, el cliente da por supuesto que no hay ningún autenticador presente en la red.</span><span class="sxs-lookup"><span data-stu-id="3306b-175">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="3306b-176">Para obtener más información, vea el [**elemento authPeriod (Onex)**](onexschema-authperiod-onex-element.md) en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-176">For more information, see the [**authPeriod (OneX) Element**](onexschema-authperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-177">**dwStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="3306b-177">**dwStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-178">El elemento startPeriod en el esquema 802.1 X que especifica el período de tiempo, en segundos, que hay que esperar antes de que se envíe un EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="3306b-178">The startPeriod element in the 802.1X schema that specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="3306b-179">Se envía un mensaje de EAPOL-Start para iniciar el proceso de autenticación de 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="3306b-179">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span> <span data-ttu-id="3306b-180">Para obtener más información, vea el [**elemento startPeriod (Onex)**](onexschema-startperiod-onex-element.md) en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-180">For more information, see the [**startPeriod (OneX) Element**](onexschema-startperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-181">**dwMaxStart**</span><span class="sxs-lookup"><span data-stu-id="3306b-181">**dwMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-182">El elemento maxStart en el esquema 802.1 X que especifica el número máximo de mensajes EAPOL-Start enviados.</span><span class="sxs-lookup"><span data-stu-id="3306b-182">The maxStart element in the 802.1X schema that specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="3306b-183">Una vez enviado el número máximo de mensajes EAPOL-Start, el cliente supone que no hay ningún autenticador presente en la red.</span><span class="sxs-lookup"><span data-stu-id="3306b-183">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="3306b-184">Para obtener más información, vea el [**elemento maxStart (Onex)**](onexschema-maxstart-onex-element.md) en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-184">For more information, see the [**maxStart (OneX) Element**](onexschema-maxstart-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-185">**dwMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="3306b-185">**dwMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-186">El elemento maxAuthFailures en el esquema 802.1 X que especifica el número máximo de errores de autenticación permitido para un conjunto de credenciales.</span><span class="sxs-lookup"><span data-stu-id="3306b-186">The maxAuthFailures element in the 802.1X schema that specifies the maximum number of authentication failures allowed for a set of credentials.</span></span> <span data-ttu-id="3306b-187">Para obtener más información, vea el elemento [**maxAuthFailures (Onex)**](onexschema-maxauthfailures-onex-element.md) en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-187">For more information, see the [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-188">**dwNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="3306b-188">**dwNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-189">Tiempo, en segundos, que se va a esperar a que se complete la autenticación de 802.1 X antes de que continúe el inicio de sesión normal.</span><span class="sxs-lookup"><span data-stu-id="3306b-189">The time, in seconds, to wait for 802.1X authentication completion before normal logon proceeds.</span></span> <span data-ttu-id="3306b-190">Este valor se usa en escenarios de inicio de sesión único (SSO).</span><span class="sxs-lookup"><span data-stu-id="3306b-190">This value is used in single signon (SSO) scenarios.</span></span> <span data-ttu-id="3306b-191">El valor predeterminado es 10 segundos en un perfil de 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="3306b-191">This value defaults to 10 seconds in an 802.1X profile.</span></span> <span data-ttu-id="3306b-192">Para obtener más información, vea el [**elemento maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md) en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-192">For more information, see the [**maxDelay (singleSignOn) Element**](onexschema-maxdelay-singlesignon-element.md) in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-193">**dwNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="3306b-193">**dwNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-194">Tiempo de espera máximo, en segundos, que se debe esperar para una conexión en caso de que se muestre un cuadro de diálogo de la interfaz de usuario que requiera la intervención del usuario durante el inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="3306b-194">The maximum duration time, in seconds, to wait for a connection in case a user interface dialog box that requires user input is displayed during the per-logon SSO.</span></span>

<span data-ttu-id="3306b-195">En Windows Vista con SP1 y versiones posteriores, este valor está codificado en 10 minutos y no es configurable.</span><span class="sxs-lookup"><span data-stu-id="3306b-195">On Windows Vista with SP1 and later, this value is hardcoded to 10 minutes and is not configurable.</span></span> <span data-ttu-id="3306b-196">En la versión de Windows Vista a fabricación, este valor tiene como valor predeterminado 60 segundos en un perfil de 802.1 X y se controla mediante el elemento **maxDelayWithAdditionalDialogs** en el esquema.</span><span class="sxs-lookup"><span data-stu-id="3306b-196">On Windows Vista Release to Manufacturing, this value defaults to 60 seconds in an 802.1X profile and was controlled by the **maxDelayWithAdditionalDialogs** element in the schema.</span></span>

<span data-ttu-id="3306b-197">En Windows Vista con SP1 y versiones posteriores, el elemento **maxDelayWithAdditionalDialogs** del esquema 802.1 x se omite y se deja en desuso.</span><span class="sxs-lookup"><span data-stu-id="3306b-197">On Windows Vista with SP1 and later, the **maxDelayWithAdditionalDialogs** element in the 802.1X schema is ignored and deprecated.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-198">**bAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="3306b-198">**bAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-199">Valor que especifica si se permiten mostrar cuadros de diálogo EAP cuando se usa el inicio de sesión único de SSO.</span><span class="sxs-lookup"><span data-stu-id="3306b-199">A value that specifies whether to allow EAP dialogs to be displayed when using pre-logon SSO.</span></span> <span data-ttu-id="3306b-200">Para obtener más información, vea el elemento **allowAdditionalDialogs** en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-200">For more information, see the **allowAdditionalDialogs** element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="3306b-201">**bUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="3306b-201">**bUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="3306b-202">El elemento userBasedVirtualLan en el esquema 802.1 X que especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="3306b-202">The userBasedVirtualLan element in the 802.1X schema that specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="3306b-203">Algunos dispositivos del servidor de acceso a la red (NAS) cambian la VLAN después de que un usuario se autentique.</span><span class="sxs-lookup"><span data-stu-id="3306b-203">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="3306b-204">Cuando userBasedVirtualLan es TRUE, el NAS puede cambiar la VLAN de un dispositivo después de que un usuario se autentique.</span><span class="sxs-lookup"><span data-stu-id="3306b-204">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span> <span data-ttu-id="3306b-205">Para obtener más información, vea el [**elemento userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) en el esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-205">For more information, see the [**userBasedVirtualLan (singleSignOn) Element**](onexschema-userbasedvirtuallan-singlesignon-element.md) in the 802.1X scheme.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3306b-206">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3306b-206">Remarks</span></span>

<span data-ttu-id="3306b-207">La estructura de **\_ \_ Perfil de conexión Onex** la usa el módulo 802.1 x, un nuevo componente de configuración inalámbrica compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3306b-207">The **ONEX\_CONNECTION\_PROFILE** structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and later.</span></span>

<span data-ttu-id="3306b-208">Los [**\_ datos de \_ actualización \_ de resultados de Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contienen información sobre un cambio de estado para la autenticación de 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-208">The [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contains information on a status change to 802.1X authentication.</span></span> <span data-ttu-id="3306b-209">La estructura de **datos de \_ \_ actualización \_ de resultados Onex** se devuelve cuando el miembro **NotificationSource** de la estructura de [**datos de \_ notificación \_ de WLAN**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) es  Onex de **origen de notificación de WLAN \_ \_ \_** y el miembro NotificationCode de la estructura de **datos de \_ notificación \_ de WLAN** para la notificación recibida es **OneXNotificationTypeResultUpdate**.</span><span class="sxs-lookup"><span data-stu-id="3306b-209">The **ONEX\_RESULT\_UPDATE\_DATA** structure is returned when the **NotificationSource** member of the [**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) structure is **WLAN\_NOTIFICATION\_SOURCE\_ONEX** and the **NotificationCode** member of the **WLAN\_NOTIFICATION\_DATA** structure for received notification is **OneXNotificationTypeResultUpdate**.</span></span> <span data-ttu-id="3306b-210">En esta notificación, el miembro **pdata** de la estructura de **\_ \_ datos de notificación de WLAN** apunta a una estructura de **\_ \_ \_ datos de actualización de resultados Onex** que contiene información sobre el cambio de estado de autenticación de 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="3306b-210">For this notification, the **pData** member of the **WLAN\_NOTIFICATION\_DATA** structure points to an **ONEX\_RESULT\_UPDATE\_DATA** structure that contains information on the 802.1X authentication status change.</span></span>

<span data-ttu-id="3306b-211">Si se establece el miembro **fOneXAuthParams** de la estructura de [**datos de \_ \_ actualización \_ de resultados Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) , el miembro **authParams** de la estructura de **datos de \_ \_ actualización \_ de resultados Onex** contiene una estructura de [**\_ \_ BLOB de variable Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) con una estructura de [**\_ \_ parámetros de autenticación Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) insertada a partir del miembro **dwOffset** del BLOB de la **\_ variable \_ Onex**.</span><span class="sxs-lookup"><span data-stu-id="3306b-211">If the **fOneXAuthParams** member in the [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) structure is set, then the **authParams** member of the **ONEX\_RESULT\_UPDATE\_DATA** structure contains an [**ONEX\_VARIABLE\_BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) structure with an [**ONEX\_AUTH\_PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span> <span data-ttu-id="3306b-212">El **miembro oneXConnProfile** de la estructura de **\_ \_ parámetros de autenticación Onex** contiene una estructura de **\_ \_ BLOB de variable Onex** con una estructura de **\_ \_ Perfil de conexión Onex** insertada a partir del miembro **dwOffset** del BLOB de la **\_ variable \_ Onex**.</span><span class="sxs-lookup"><span data-stu-id="3306b-212">The **oneXConnProfile** member of the **ONEX\_AUTH\_PARAMS** structure contains an **ONEX\_VARIABLE\_BLOB** structure with an **ONEX\_CONNECTION\_PROFILE** structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span>

<span data-ttu-id="3306b-213">La estructura de **\_ \_ Perfil de conexión Onex** no está definida en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="3306b-213">The **ONEX\_CONNECTION\_PROFILE** structure is not defined in a public header file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3306b-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3306b-214">Requirements</span></span>



| <span data-ttu-id="3306b-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="3306b-215">Requirement</span></span> | <span data-ttu-id="3306b-216">Value</span><span class="sxs-lookup"><span data-stu-id="3306b-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3306b-217">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3306b-217">Minimum supported client</span></span><br/> | <span data-ttu-id="3306b-218">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3306b-218">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3306b-219">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3306b-219">Minimum supported server</span></span><br/> | <span data-ttu-id="3306b-220">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3306b-220">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3306b-221">Vea también</span><span class="sxs-lookup"><span data-stu-id="3306b-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3306b-222">Acerca de la arquitectura ACM</span><span class="sxs-lookup"><span data-stu-id="3306b-222">About the ACM Architecture</span></span>](about-the-acm-architecture.md)
</dt> <dt>

[<span data-ttu-id="3306b-223">Esquema OneX</span><span class="sxs-lookup"><span data-stu-id="3306b-223">OneX Schema</span></span>](onexschema-schema.md)
</dt> <dt>

[<span data-ttu-id="3306b-224">**Elemento authMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="3306b-224">**authMode (OneX) Element**</span></span>](onexschema-authmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="3306b-225">**Elemento authPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="3306b-225">**authPeriod (OneX) Element**</span></span>](onexschema-authperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="3306b-226">**Elemento heldPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="3306b-226">**heldPeriod (OneX) Element**</span></span>](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="3306b-227">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="3306b-227">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[<span data-ttu-id="3306b-228">**Elemento maxStart (OneX)**</span><span class="sxs-lookup"><span data-stu-id="3306b-228">**maxStart (OneX) Element**</span></span>](onexschema-maxstart-onex-element.md)
</dt> <dt>

[<span data-ttu-id="3306b-229">**Elemento startPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="3306b-229">**startPeriod (OneX) Element**</span></span>](onexschema-startperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="3306b-230">**Elemento supplicantMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="3306b-230">**supplicantMode (OneX) Element**</span></span>](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="3306b-231">**Elemento userBasedVirtualLan (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="3306b-231">**userBasedVirtualLan (singleSignOn) Element**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[<span data-ttu-id="3306b-232">**\_parámetros de autenticación Onex \_**</span><span class="sxs-lookup"><span data-stu-id="3306b-232">**ONEX\_AUTH\_PARAMS**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[<span data-ttu-id="3306b-233">**\_tipo de notificación Onex \_**</span><span class="sxs-lookup"><span data-stu-id="3306b-233">**ONEX\_NOTIFICATION\_TYPE**</span></span>](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[<span data-ttu-id="3306b-234">**\_datos de \_ actualización de resultados de Onex \_**</span><span class="sxs-lookup"><span data-stu-id="3306b-234">**ONEX\_RESULT\_UPDATE\_DATA**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[<span data-ttu-id="3306b-235">**OneX (elemento de esquema)**</span><span class="sxs-lookup"><span data-stu-id="3306b-235">**OneX Schema Element**</span></span>](onexschema-onex-element.md)
</dt> <dt>

[<span data-ttu-id="3306b-236">**\_BLOB de variable de Onex \_**</span><span class="sxs-lookup"><span data-stu-id="3306b-236">**ONEX\_VARIABLE\_BLOB**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

<span data-ttu-id="3306b-237">[**\_datos de notificación de WLAN \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3306b-237">[**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3306b-238">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="3306b-238">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
