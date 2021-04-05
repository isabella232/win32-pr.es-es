---
title: Clase MDM_Policy_Config01_Privacy02
description: La \_ clase Config01 de Privacy02 de directivas MDM \_ \_ representa las directivas de búsqueda disponibles.
ms.assetid: 202213b9-5301-4c55-bbc6-6ce3daf705ad
keywords:
- Clase MDM_Policy_Config01_Privacy02
- MDM_Policy_Config01_Privacy02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Privacy02
- MDM_Policy_Config01_Privacy02.InstanceID
- MDM_Policy_Config01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca714dc17db60982e5ba047690886bc88aa79853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996371"
---
# <a name="mdm_policy_config01_privacy02-class"></a><span data-ttu-id="f2438-105">\_ \_ Clase Privacy02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="f2438-105">MDM\_Policy\_Config01\_Privacy02 class</span></span>

<span data-ttu-id="f2438-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="f2438-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f2438-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="f2438-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f2438-108">La **clase \_ \_ Config01 de \_ Privacy02 de directivas MDM** representa las directivas de búsqueda disponibles.</span><span class="sxs-lookup"><span data-stu-id="f2438-108">The **MDM\_Policy\_Config01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="f2438-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f2438-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2438-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2438-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Privacy02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAutoAcceptPairingAndPrivacyConsentPrompts;
  sint32 AllowInputPersonalization;
  string LetAppsSyncWithDevices_UserInControlOfTheseApps;
  sint32 PublishUserActivities;
  string LetAppsSyncWithDevices_ForceDenyTheseApps;
  string LetAppsSyncWithDevices_ForceAllowTheseApps;
  sint32 LetAppsSyncWithDevices;
  string LetAppsAccessTrustedDevices_UserInControlOfTheseApps;
  string LetAppsRunInBackground_UserInControlOfTheseApps;
  string LetAppsRunInBackground_ForceDenyTheseApps;
  string LetAppsRunInBackground_ForceAllowTheseApps;
  sint32 LetAppsRunInBackground;
  string LetAppsGetDiagnosticInfo_UserInControlOfTheseApps;
  string LetAppsGetDiagnosticInfo_ForceDenyTheseApps;
  string LetAppsGetDiagnosticInfo_ForceAllowTheseApps;
  sint32 LetAppsGetDiagnosticInfo;
  string LetAppsAccessTrustedDevices_ForceDenyTheseApps;
  string LetAppsAccessTrustedDevices_ForceAllowTheseApps;
  sint32 LetAppsAccessTrustedDevices;
  string LetAppsAccessRadios_UserInControlOfTheseApps;
  string LetAppsAccessTasks_UserInControlOfTheseApps;
  string LetAppsAccessTasks_ForceDenyTheseApps;
  string LetAppsAccessTasks_ForceAllowTheseApps;
  sint32 LetAppsAccessTasks;
  string LetAppsAccessRadios_ForceDenyTheseApps;
  string LetAppsAccessRadios_ForceAllowTheseApps;
  sint32 LetAppsAccessRadios;
  string LetAppsAccessPhone_UserInControlOfTheseApps;
  string LetAppsAccessPhone_ForceDenyTheseApps;
  string LetAppsAccessPhone_ForceAllowTheseApps;
  sint32 LetAppsAccessPhone;
  string LetAppsAccessMotion_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_ForceDenyTheseApps;
  string LetAppsAccessNotifications_ForceAllowTheseApps;
  sint32 LetAppsAccessNotifications;
  string LetAppsAccessMotion_ForceDenyTheseApps;
  string LetAppsAccessMotion_ForceAllowTheseApps;
  sint32 LetAppsAccessMotion;
  string LetAppsAccessMicrophone_UserInControlOfTheseApps;
  string LetAppsAccessMicrophone_ForceDenyTheseApps;
  string LetAppsAccessMicrophone_ForceAllowTheseApps;
  sint32 LetAppsAccessMicrophone;
  string LetAppsAccessMessaging_UserInControlOfTheseApps;
  string LetAppsAccessMessaging_ForceDenyTheseApps;
  string LetAppsAccessMessaging_ForceAllowTheseApps;
  sint32 LetAppsAccessMessaging;
  string LetAppsAccessLocation_UserInControlOfTheseApps;
  string LetAppsAccessLocation_ForceDenyTheseApps;
  string LetAppsAccessLocation_ForceAllowTheseApps;
  sint32 LetAppsAccessLocation;
  string LetAppsAccessEmail_UserInControlOfTheseApps;
  string LetAppsAccessEmail_ForceDenyTheseApps;
  string LetAppsAccessEmail_ForceAllowTheseApps;
  sint32 LetAppsAccessEmail;
  string LetAppsAccessContacts_UserInControlOfTheseApps;
  string LetAppsAccessContacts_ForceDenyTheseApps;
  string LetAppsAccessContacts_ForceAllowTheseApps;
  sint32 LetAppsAccessContacts;
  string LetAppsAccessCamera_UserInControlOfTheseApps;
  string LetAppsAccessCamera_ForceDenyTheseApps;
  string LetAppsAccessCamera_ForceAllowTheseApps;
  sint32 LetAppsAccessCamera;
  string LetAppsAccessCallHistory_UserInControlOfTheseApps;
  string LetAppsAccessCallHistory_ForceDenyTheseApps;
  string LetAppsAccessCallHistory_ForceAllowTheseApps;
  sint32 LetAppsAccessCallHistory;
  string LetAppsAccessCalendar_UserInControlOfTheseApps;
  string LetAppsAccessCalendar_ForceDenyTheseApps;
  string LetAppsAccessCalendar_ForceAllowTheseApps;
  sint32 LetAppsAccessCalendar;
  string LetAppsAccessAccountInfo_UserInControlOfTheseApps;
  string LetAppsAccessAccountInfo_ForceDenyTheseApps;
  string LetAppsAccessAccountInfo_ForceAllowTheseApps;
  sint32 LetAppsAccessAccountInfo;
  sint32 DisableAdvertisingId;
  sint32 EnableActivityFeed;
};
```

## <a name="members"></a><span data-ttu-id="f2438-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f2438-111">Members</span></span>

<span data-ttu-id="f2438-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Privacy02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f2438-112">The **MDM\_Policy\_Config01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="f2438-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2438-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2438-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2438-114">Properties</span></span>

<span data-ttu-id="f2438-115">La **clase \_ \_ Config01 de \_ Privacy02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f2438-115">The **MDM\_Policy\_Config01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f2438-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span><span class="sxs-lookup"><span data-stu-id="f2438-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-119">AllowInputPersonalization</span><span class="sxs-lookup"><span data-stu-id="f2438-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-122">DisableAdvertisingId</span><span class="sxs-lookup"><span data-stu-id="f2438-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-125">EnableActivityFeed</span><span class="sxs-lookup"><span data-stu-id="f2438-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2438-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f2438-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2438-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2438-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2438-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2438-132">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="f2438-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="f2438-133">Para esta clase, la cadena es "Privacy".</span><span class="sxs-lookup"><span data-stu-id="f2438-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="f2438-134">LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="f2438-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-137">LetAppsAccessAccountInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-140">LetAppsAccessAccountInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-143">LetAppsAccessAccountInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-146">LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="f2438-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-149">LetAppsAccessCalendar \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-152">LetAppsAccessCalendar \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-155">LetAppsAccessCalendar \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-158">LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="f2438-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-161">LetAppsAccessCallHistory \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-164">LetAppsAccessCallHistory \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-167">LetAppsAccessCallHistory \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-170">LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="f2438-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-171">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-173">LetAppsAccessCamera \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-176">LetAppsAccessCamera \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-179">LetAppsAccessCamera \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-182">LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="f2438-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-183">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-185">LetAppsAccessContacts \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-188">LetAppsAccessContacts \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-191">LetAppsAccessContacts \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-194">LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="f2438-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-195">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-196">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-197">LetAppsAccessEmail \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-200">LetAppsAccessEmail \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-203">LetAppsAccessEmail \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-205">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-206">LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="f2438-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-207">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-209">LetAppsAccessLocation \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-212">LetAppsAccessLocation \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-215">LetAppsAccessLocation \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-218">LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="f2438-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-219">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-221">LetAppsAccessMessaging \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-224">LetAppsAccessMessaging \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-227">LetAppsAccessMessaging \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-230">LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="f2438-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-231">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-233">LetAppsAccessMicrophone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-235">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-236">LetAppsAccessMicrophone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-238">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-239">LetAppsAccessMicrophone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-241">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-242">LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="f2438-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-243">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-244">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-245">LetAppsAccessMotion \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-247">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-248">LetAppsAccessMotion \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-250">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-251">LetAppsAccessMotion \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-254">LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="f2438-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-255">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-256">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-257">LetAppsAccessNotifications \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-259">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-260">LetAppsAccessNotifications \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-263">LetAppsAccessNotifications \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-265">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-266">LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="f2438-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-267">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-268">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-269">LetAppsAccessPhone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-271">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-272">LetAppsAccessPhone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-274">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-275">LetAppsAccessPhone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-277">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-278">LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="f2438-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-279">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-280">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-281">LetAppsAccessRadios \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-283">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-284">LetAppsAccessRadios \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-285">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-286">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-287">LetAppsAccessRadios \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-289">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-290">LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="f2438-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-291">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-292">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-293">LetAppsAccessTasks \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-295">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-296">LetAppsAccessTasks \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-298">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-299">LetAppsAccessTasks \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-301">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-302">LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="f2438-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-303">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-304">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-305">LetAppsAccessTrustedDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-306">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-307">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-308">LetAppsAccessTrustedDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-310">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-311">LetAppsAccessTrustedDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-313">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-314">LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="f2438-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-315">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-316">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-317">LetAppsGetDiagnosticInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-318">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-319">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-320">LetAppsGetDiagnosticInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-322">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-323">LetAppsGetDiagnosticInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-325">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-326">LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="f2438-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-327">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-328">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-329">LetAppsRunInBackground \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-331">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-332">LetAppsRunInBackground \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-334">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-335">LetAppsRunInBackground \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-336">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-337">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-338">LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="f2438-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-339">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-340">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-341">LetAppsSyncWithDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-343">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-344">LetAppsSyncWithDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-345">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-346">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2438-347">LetAppsSyncWithDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="f2438-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-348">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-349">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2438-350">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f2438-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-351">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2438-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2438-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2438-353">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2438-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2438-354">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="f2438-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="f2438-355">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="f2438-355">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="f2438-356">PublishUserActivities</span><span class="sxs-lookup"><span data-stu-id="f2438-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2438-357">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2438-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2438-358">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2438-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2438-359">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2438-359">Requirements</span></span>



| <span data-ttu-id="f2438-360">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2438-360">Requirement</span></span> | <span data-ttu-id="f2438-361">Value</span><span class="sxs-lookup"><span data-stu-id="f2438-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2438-362">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2438-362">Minimum supported client</span></span><br/> | <span data-ttu-id="f2438-363">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2438-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2438-364">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2438-364">Minimum supported server</span></span><br/> | <span data-ttu-id="f2438-365">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f2438-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f2438-366">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f2438-366">Namespace</span></span><br/>                | <span data-ttu-id="f2438-367">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="f2438-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f2438-368">MOF</span><span class="sxs-lookup"><span data-stu-id="f2438-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2438-369"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2438-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2438-370">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2438-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2438-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2438-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2438-372">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2438-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2438-373">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="f2438-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

