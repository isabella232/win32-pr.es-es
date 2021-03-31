---
title: MDM_Policy_Config01_LocalPoliciesSecurityOptions02 (clase)
description: La \_ Directiva MDM \_ Config01 \_ LocalPoliciesSecurityOptions02 configura las opciones de seguridad de las directivas locales.
ms.assetid: 07688109-f14a-4a04-91b2-ee928d8911b4
keywords:
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02 (clase)
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02.InstanceID
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf39e1db2f5d6f823667865054a8c72b18dc916f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079350"
---
# <a name="mdm_policy_config01_localpoliciessecurityoptions02-class"></a><span data-ttu-id="b72f2-105">\_ \_ Clase LocalPoliciesSecurityOptions02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="b72f2-105">MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02 class</span></span>

<span data-ttu-id="b72f2-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b72f2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b72f2-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b72f2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b72f2-108">La \_ Directiva MDM \_ Config01 \_ LocalPoliciesSecurityOptions02 configura las opciones de seguridad de las directivas locales.</span><span class="sxs-lookup"><span data-stu-id="b72f2-108">The MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02 configures the local policies security options.</span></span>

<span data-ttu-id="b72f2-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b72f2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b72f2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b72f2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_LocalPoliciesSecurityOptions02
{
  string InstanceID;
  string ParentID;
  sint32 Accounts_BlockMicrosoftAccounts;
  sint32 Accounts_EnableGuestAccountStatus;
  sint32 Accounts_EnableAdministratorAccountStatus;
  sint32 Accounts_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly;
  string Accounts_RenameAdministratorAccount;
  string Accounts_RenameGuestAccount;
  string Devices_RestrictCDROMAccessToLocallyLoggedOnUserOnly;
  sint32 Devices_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters;
  sint32 Devices_AllowUndockWithoutHavingToLogon;
  string Devices_AllowedToFormatAndEjectRemovableMedia;
  sint32 InteractiveLogon_DisplayUserInformationWhenTheSessionIsLocked;
  sint32 Interactivelogon_DoNotDisplayLastSignedIn;
  sint32 Interactivelogon_DoNotDisplayUsernameAtSignIn;
  sint32 Interactivelogon_DoNotRequireCTRLALTDEL;
  sint32 InteractiveLogon_MachineInactivityLimit;
  string InteractiveLogon_MessageTextForUsersAttemptingToLogOn;
  string InteractiveLogon_MessageTitleForUsersAttemptingToLogOn;
  sint32 NetworkAccess_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares;
  sint32 NetworkAccess_RestrictAnonymousAccessToNamedPipesAndShares;
  string NetworkAccess_RestrictClientsAllowedToMakeRemoteCallsToSAM;
  sint32 NetworkSecurity_AllowPKU2UAuthenticationRequests;
  sint32 RecoveryConsole_AllowAutomaticAdministrativeLogon;
  sint32 Shutdown_AllowSystemToBeShutDownWithoutHavingToLogOn;
  sint32 Shutdown_ClearVirtualMemoryPageFile;
  sint32 UserAccountControl_AllowUIAccessApplicationsToPromptForElevation;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForAdministrators;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForStandardUsers;
  sint32 UserAccountControl_DetectApplicationInstallationsAndPromptForElevation;
  sint32 UserAccountControl_OnlyElevateExecutableFilesThatAreSignedAndValidated;
  sint32 UserAccountControl_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations;
  sint32 UserAccountControl_RunAllAdministratorsInAdminApprovalMode;
  sint32 UserAccountControl_SwitchToTheSecureDesktopWhenPromptingForElevation;
  sint32 UserAccountControl_UseAdminApprovalMode;
  sint32 UserAccountControl_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations;
};
```

## <a name="members"></a><span data-ttu-id="b72f2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b72f2-111">Members</span></span>

<span data-ttu-id="b72f2-112">La clase Config01 de la **\_ Directiva MDM \_ \_ LocalPoliciesSecurityOptions02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b72f2-112">The **MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02** class has these types of members:</span></span>

-   [<span data-ttu-id="b72f2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b72f2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b72f2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b72f2-114">Properties</span></span>

<span data-ttu-id="b72f2-115">La **clase \_ \_ Config01 de \_ LocalPoliciesSecurityOptions02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b72f2-115">The **MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b72f2-116">Cuentas \_ BlockMicrosoftAccounts</span><span class="sxs-lookup"><span data-stu-id="b72f2-116">Accounts\_BlockMicrosoftAccounts</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b72f2-119">Accounts_EnableAdministratorAccountStatus</span><span class="sxs-lookup"><span data-stu-id="b72f2-119">Accounts_EnableAdministratorAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b72f2-122">Accounts_EnableGuestAccountStatus</span><span class="sxs-lookup"><span data-stu-id="b72f2-122">Accounts_EnableGuestAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-125">Cuentas \_ LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span><span class="sxs-lookup"><span data-stu-id="b72f2-125">Accounts\_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-128">Cuentas \_ RenameAdministratorAccount</span><span class="sxs-lookup"><span data-stu-id="b72f2-128">Accounts\_RenameAdministratorAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b72f2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-131">Cuentas \_ RenameGuestAccount</span><span class="sxs-lookup"><span data-stu-id="b72f2-131">Accounts\_RenameGuestAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b72f2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-134">Dispositivos \_ AllowedToFormatAndEjectRemovableMedia</span><span class="sxs-lookup"><span data-stu-id="b72f2-134">Devices\_AllowedToFormatAndEjectRemovableMedia</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b72f2-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-137">Dispositivos \_ AllowUndockWithoutHavingToLogon</span><span class="sxs-lookup"><span data-stu-id="b72f2-137">Devices\_AllowUndockWithoutHavingToLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-140">Dispositivos \_ PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span><span class="sxs-lookup"><span data-stu-id="b72f2-140">Devices\_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-143">Dispositivos \_ RestrictCDROMAccessToLocallyLoggedOnUserOnly</span><span class="sxs-lookup"><span data-stu-id="b72f2-143">Devices\_RestrictCDROMAccessToLocallyLoggedOnUserOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b72f2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b72f2-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b72f2-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b72f2-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b72f2-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-149">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b72f2-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-150">InteractiveLogon \_ DisplayUserInformationWhenTheSessionIsLocked</span><span class="sxs-lookup"><span data-stu-id="b72f2-150">InteractiveLogon\_DisplayUserInformationWhenTheSessionIsLocked</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-151">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-153">Interactivelogon \_ DoNotDisplayLastSignedIn</span><span class="sxs-lookup"><span data-stu-id="b72f2-153">Interactivelogon\_DoNotDisplayLastSignedIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-154">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-156">Interactivelogon \_ DoNotDisplayUsernameAtSignIn</span><span class="sxs-lookup"><span data-stu-id="b72f2-156">Interactivelogon\_DoNotDisplayUsernameAtSignIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-157">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-159">Interactivelogon \_ DoNotRequireCTRLALTDEL</span><span class="sxs-lookup"><span data-stu-id="b72f2-159">Interactivelogon\_DoNotRequireCTRLALTDEL</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-160">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-161">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-162">InteractiveLogon \_ MachineInactivityLimit</span><span class="sxs-lookup"><span data-stu-id="b72f2-162">InteractiveLogon\_MachineInactivityLimit</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-163">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-164">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-165">InteractiveLogon \_ MessageTextForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="b72f2-165">InteractiveLogon\_MessageTextForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b72f2-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-167">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-168">InteractiveLogon \_ MessageTitleForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="b72f2-168">InteractiveLogon\_MessageTitleForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b72f2-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-171">NetworkAccess \_ DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span><span class="sxs-lookup"><span data-stu-id="b72f2-171">NetworkAccess\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-172">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-174">NetworkAccess \_ RestrictAnonymousAccessToNamedPipesAndShares</span><span class="sxs-lookup"><span data-stu-id="b72f2-174">NetworkAccess\_RestrictAnonymousAccessToNamedPipesAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-175">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-176">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-177">NetworkAccess \_ RestrictClientsAllowedToMakeRemoteCallsToSAM</span><span class="sxs-lookup"><span data-stu-id="b72f2-177">NetworkAccess\_RestrictClientsAllowedToMakeRemoteCallsToSAM</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b72f2-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-179">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-180">NetworkSecurity \_ AllowPKU2UAuthenticationRequests</span><span class="sxs-lookup"><span data-stu-id="b72f2-180">NetworkSecurity\_AllowPKU2UAuthenticationRequests</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-181">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-182">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b72f2-183">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b72f2-183">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b72f2-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b72f2-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-186">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b72f2-186">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-187">RecoveryConsole \_ AllowAutomaticAdministrativeLogon</span><span class="sxs-lookup"><span data-stu-id="b72f2-187">RecoveryConsole\_AllowAutomaticAdministrativeLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-188">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-188">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-189">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-190">Cerrar \_ AllowSystemToBeShutDownWithoutHavingToLogOn</span><span class="sxs-lookup"><span data-stu-id="b72f2-190">Shutdown\_AllowSystemToBeShutDownWithoutHavingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-191">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-191">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-192">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-193">Cerrar \_ ClearVirtualMemoryPageFile</span><span class="sxs-lookup"><span data-stu-id="b72f2-193">Shutdown\_ClearVirtualMemoryPageFile</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-194">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-194">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-195">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-196">UserAccountControl \_ AllowUIAccessApplicationsToPromptForElevation</span><span class="sxs-lookup"><span data-stu-id="b72f2-196">UserAccountControl\_AllowUIAccessApplicationsToPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-197">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-197">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-198">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-199">UserAccountControl \_ BehaviorOfTheElevationPromptForAdministrators</span><span class="sxs-lookup"><span data-stu-id="b72f2-199">UserAccountControl\_BehaviorOfTheElevationPromptForAdministrators</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-200">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-201">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-202">UserAccountControl \_ BehaviorOfTheElevationPromptForStandardUsers</span><span class="sxs-lookup"><span data-stu-id="b72f2-202">UserAccountControl\_BehaviorOfTheElevationPromptForStandardUsers</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-203">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-203">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-204">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-205">UserAccountControl \_ DetectApplicationInstallationsAndPromptForElevation</span><span class="sxs-lookup"><span data-stu-id="b72f2-205">UserAccountControl\_DetectApplicationInstallationsAndPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-206">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-206">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-207">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-208">UserAccountControl \_ OnlyElevateExecutableFilesThatAreSignedAndValidated</span><span class="sxs-lookup"><span data-stu-id="b72f2-208">UserAccountControl\_OnlyElevateExecutableFilesThatAreSignedAndValidated</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-209">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-210">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-210">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-211">UserAccountControl \_ OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span><span class="sxs-lookup"><span data-stu-id="b72f2-211">UserAccountControl\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-212">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-212">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-213">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-213">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-214">UserAccountControl \_ RunAllAdministratorsInAdminApprovalMode</span><span class="sxs-lookup"><span data-stu-id="b72f2-214">UserAccountControl\_RunAllAdministratorsInAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-215">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-216">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-216">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-217">UserAccountControl \_ SwitchToTheSecureDesktopWhenPromptingForElevation</span><span class="sxs-lookup"><span data-stu-id="b72f2-217">UserAccountControl\_SwitchToTheSecureDesktopWhenPromptingForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-218">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-218">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-219">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-219">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-220">UserAccountControl \_ UseAdminApprovalMode</span><span class="sxs-lookup"><span data-stu-id="b72f2-220">UserAccountControl\_UseAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-221">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-221">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-222">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-222">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b72f2-223">UserAccountControl \_ VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span><span class="sxs-lookup"><span data-stu-id="b72f2-223">UserAccountControl\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b72f2-224">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b72f2-224">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b72f2-225">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b72f2-225">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b72f2-226">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b72f2-226">Requirements</span></span>



| <span data-ttu-id="b72f2-227">Requisito</span><span class="sxs-lookup"><span data-stu-id="b72f2-227">Requirement</span></span> | <span data-ttu-id="b72f2-228">Value</span><span class="sxs-lookup"><span data-stu-id="b72f2-228">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b72f2-229">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b72f2-229">Minimum supported client</span></span><br/> | <span data-ttu-id="b72f2-230">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b72f2-230">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b72f2-231">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b72f2-231">Minimum supported server</span></span><br/> | <span data-ttu-id="b72f2-232">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b72f2-232">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b72f2-233">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b72f2-233">Namespace</span></span><br/>                | <span data-ttu-id="b72f2-234">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b72f2-234">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b72f2-235">MOF</span><span class="sxs-lookup"><span data-stu-id="b72f2-235">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b72f2-236"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b72f2-236"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b72f2-237">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b72f2-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b72f2-238"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b72f2-238"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

