---
title: Clase MDM_Policy_User_Result01_InternetExplorer02
description: La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ InternetExplorer02 representa las directivas disponibles de Internet Explorer.
ms.assetid: efd999aa-4aa8-486d-82d4-20af7e2005fe
keywords:
- Clase MDM_Policy_User_Result01_InternetExplorer02
- MDM_Policy_User_Result01_InternetExplorer02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_InternetExplorer02
- MDM_Policy_User_Result01_InternetExplorer02.InstanceID
- MDM_Policy_User_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8693720c7a973cc6bc689abbf76a4674f185e23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489202"
---
# <a name="mdm_policy_user_result01_internetexplorer02-class"></a><span data-ttu-id="36de4-105">\_Clase InternetExplorer02 de usuario de directiva MDM \_ \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="36de4-105">MDM\_Policy\_User\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="36de4-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="36de4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="36de4-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="36de4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="36de4-108">La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ InternetExplorer02 representa las directivas disponibles de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="36de4-108">The MDM\_Policy\_User\_Result01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="36de4-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="36de4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="36de4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36de4-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowAutoComplete;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowInternetExplorer7PolicyList;
  string AllowInternetExplorerStandardsMode;
  string AllowInternetZoneTemplate;
  string AllowIntranetZoneTemplate;
  string AllowLocalMachineZoneTemplate;
  string AllowLockedDownInternetZoneTemplate;
  string AllowLockedDownIntranetZoneTemplate;
  string AllowLockedDownLocalMachineZoneTemplate;
  string AllowLockedDownRestrictedSitesZoneTemplate;
  string AllowOneWordEntry;
  string AllowSiteToZoneAssignmentList;
  string AllowsLockedDownTrustedSitesZoneTemplate;
  string AllowSoftwareWhenSignatureIsInvalid;
  string AllowsRestrictedSitesZoneTemplate;
  string AllowSuggestedSites;
  string AllowTrustedSitesZoneTemplate;
  string ConsistentMimeHandlingInternetExplorerProcesses;
  string CheckSignaturesOnDownloadedPrograms;
  string CheckServerCertificateRevocation;
  string DisableAdobeFlash;
  string DisableBlockingOfOutdatedActiveXControls;
  string DisableBypassOfSmartScreenWarnings;
  string DisableBypassOfSmartScreenWarningsAboutUncommonFiles;
  string DisableCrashDetection;
  string DisableConfiguringHistory;
  string DisableCustomerExperienceImprovementProgramParticipation;
  string DisableDeletingUserVisitedWebsites;
  string DisableEnclosureDownloading;
  string DisableEncryptionSupport;
  string DisableFirstRunWizard;
  string DisableFlipAheadFeature;
  string DisableHomePageChange;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DisableSecuritySettingsCheck;
  string DoNotBlockOutdatedActiveXControls;
  string DoNotBlockOutdatedActiveXControlsOnSpecificDomains;
  string IncludeAllLocalSites;
  string IncludeAllNetworkPaths;
  string InternetZoneAllowAccessToDataSources;
  string InternetZoneAllowAutomaticPromptingForActiveXControls;
  string InternetZoneAllowAutomaticPromptingForFileDownloads;
  string InternetZoneAllowDragAndDropCopyAndPasteFiles;
  string InternetZoneAllowCopyPasteViaScript;
  string InternetZoneAllowFontDownloads;
  string InternetZoneAllowLessPrivilegedSites;
  string InternetZoneAllowLoadingOfXAMLFiles;
  string InternetZoneAllowNETFrameworkReliantComponents;
  string InternetZoneAllowScriptInitiatedWindows;
  string InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string InternetZoneAllowScriptlets;
  string InternetZoneAllowSmartScreenIE;
  string InternetZoneAllowUpdatesToStatusBarViaScript;
  string InternetZoneAllowUserDataPersistence;
  string InternetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string InternetZoneIncludeLocalPathWhenUploadingFilesToServer;
  string InternetZoneEnableProtectedMode;
  string InternetZoneEnableMIMESniffing;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string InternetZoneEnableCrossSiteScriptingFilter;
  string InternetZoneDownloadUnsignedActiveXControls;
  string InternetZoneDownloadSignedActiveXControls;
  string InternetZoneInitializeAndScriptActiveXControls;
  string InternetZoneJavaPermissions;
  string InternetZoneLogonOptions;
  string InternetZoneLaunchingApplicationsAndFilesInIFRAME;
  string InternetZoneNavigateWindowsAndFrames;
  string InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone;
  string InternetZoneUsePopupBlocker;
  string InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode;
  string IntranetZoneAllowAccessToDataSources;
  string IntranetZoneAllowAutomaticPromptingForActiveXControls;
  string IntranetZoneAllowAutomaticPromptingForFileDownloads;
  string IntranetZoneAllowFontDownloads;
  string IntranetZoneAllowLessPrivilegedSites;
  string IntranetZoneAllowNETFrameworkReliantComponents;
  string IntranetZoneAllowScriptlets;
  string IntranetZoneAllowSmartScreenIE;
  string IntranetZoneAllowUserDataPersistence;
  string IntranetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string IntranetZoneInitializeAndScriptActiveXControls;
  string IntranetZoneJavaPermissions;
  string IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string IntranetZoneNavigateWindowsAndFrames;
  string LocalMachineZoneAllowAccessToDataSources;
  string LocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LocalMachineZoneAllowFontDownloads;
  string LocalMachineZoneAllowLessPrivilegedSites;
  string LocalMachineZoneAllowNETFrameworkReliantComponents;
  string LocalMachineZoneAllowScriptlets;
  string LocalMachineZoneAllowSmartScreenIE;
  string LocalMachineZoneAllowUserDataPersistence;
  string LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls;
  string LocalMachineZoneInitializeAndScriptActiveXControls;
  string LocalMachineZoneJavaPermissions;
  string LocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownInternetZoneAllowAccessToDataSources;
  string LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownInternetZoneAllowFontDownloads;
  string LockedDownInternetZoneAllowLessPrivilegedSites;
  string LockedDownInternetZoneAllowNETFrameworkReliantComponents;
  string LockedDownInternetZoneAllowScriptlets;
  string LockedDownInternetZoneAllowSmartScreenIE;
  string LockedDownInternetZoneAllowUserDataPersistence;
  string LockedDownInternetZoneInitializeAndScriptActiveXControls;
  string LockedDownInternetZoneJavaPermissions;
  string LockedDownInternetZoneNavigateWindowsAndFrames;
  string LockedDownIntranetZoneAllowAccessToDataSources;
  string LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownIntranetZoneAllowFontDownloads;
  string LockedDownIntranetZoneAllowLessPrivilegedSites;
  string LockedDownIntranetZoneAllowNETFrameworkReliantComponents;
  string LockedDownIntranetZoneAllowScriptlets;
  string LockedDownIntranetZoneAllowSmartScreenIE;
  string LockedDownIntranetZoneAllowUserDataPersistence;
  string LockedDownIntranetZoneInitializeAndScriptActiveXControls;
  string LockedDownIntranetZoneNavigateWindowsAndFrames;
  string LockedDownLocalMachineZoneAllowAccessToDataSources;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownLocalMachineZoneAllowFontDownloads;
  string LockedDownLocalMachineZoneAllowLessPrivilegedSites;
  string LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents;
  string LockedDownLocalMachineZoneAllowScriptlets;
  string LockedDownLocalMachineZoneAllowSmartScreenIE;
  string LockedDownLocalMachineZoneAllowUserDataPersistence;
  string LockedDownLocalMachineZoneInitializeAndScriptActiveXControls;
  string LockedDownLocalMachineZoneJavaPermissions;
  string LockedDownLocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownRestrictedSitesZoneAllowAccessToDataSources;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownRestrictedSitesZoneAllowFontDownloads;
  string LockedDownRestrictedSitesZoneAllowLessPrivilegedSites;
  string LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownRestrictedSitesZoneAllowScriptlets;
  string LockedDownRestrictedSitesZoneAllowSmartScreenIE;
  string LockedDownRestrictedSitesZoneAllowUserDataPersistence;
  string LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownRestrictedSitesZoneJavaPermissions;
  string LockedDownRestrictedSitesZoneNavigateWindowsAndFrames;
  string LockedDownTrustedSitesZoneAllowAccessToDataSources;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownTrustedSitesZoneAllowFontDownloads;
  string LockedDownTrustedSitesZoneAllowLessPrivilegedSites;
  string LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownTrustedSitesZoneAllowScriptlets;
  string LockedDownTrustedSitesZoneAllowSmartScreenIE;
  string LockedDownTrustedSitesZoneAllowUserDataPersistence;
  string LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownTrustedSitesZoneJavaPermissions;
  string LockedDownTrustedSitesZoneNavigateWindowsAndFrames;
  string RestrictActiveXInstallInternetExplorerProcesses;
  string RemoveRunThisTimeButtonForOutdatedActiveXControls;
  string ProtectionFromZoneElevationInternetExplorerProcesses;
  string PreventPerUserInstallationOfActiveXControls;
  string PreventManagingSmartScreenFilter;
  string NotificationBarInternetExplorerProcesses;
  string MKProtocolSecurityRestrictionInternetExplorerProcesses;
  string MimeSniffingSafetyFeatureInternetExplorerProcesses;
  string RestrictedSitesZoneAllowAccessToDataSources;
  string RestrictedSitesZoneAllowActiveScripting;
  string RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string RestrictedSitesZoneAllowFileDownloads;
  string RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles;
  string RestrictedSitesZoneAllowCopyPasteViaScript;
  string RestrictedSitesZoneAllowBinaryAndScriptBehaviors;
  string RestrictedSitesZoneAllowFontDownloads;
  string RestrictedSitesZoneAllowLessPrivilegedSites;
  string RestrictedSitesZoneAllowMETAREFRESH;
  string RestrictedSitesZoneAllowLoadingOfXAMLFiles;
  string RestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string RestrictedSitesZoneAllowScriptInitiatedWindows;
  string RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string RestrictedSitesZoneAllowScriptlets;
  string RestrictedSitesZoneAllowSmartScreenIE;
  string RestrictedSitesZoneAllowUpdatesToStatusBarViaScript;
  string RestrictedSitesZoneAllowUserDataPersistence;
  string RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer;
  string RestrictedSitesZoneEnableMIMESniffing;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string RestrictedSitesZoneDownloadUnsignedActiveXControls;
  string RestrictedSitesZoneEnableCrossSiteScriptingFilter;
  string RestrictedSitesZoneDownloadSignedActiveXControls;
  string RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string RestrictedSitesZoneInitializeAndScriptActiveXControls;
  string RestrictedSitesZoneLogonOptions;
  string RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME;
  string RestrictedSitesZoneJavaPermissions;
  string RestrictedSitesZoneNavigateWindowsAndFrames;
  string ScriptedWindowSecurityRestrictionsInternetExplorerProcesses;
  string RestrictFileDownloadInternetExplorerProcesses;
  string RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting;
  string RestrictedSitesZoneUsePopupBlocker;
  string RestrictedSitesZoneTurnOnProtectedMode;
  string RestrictedSitesZoneTurnOnCrossSiteScriptingFilter;
  string RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string RestrictedSitesZoneScriptingOfJavaApplets;
  string RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string RestrictedSitesZoneRunActiveXControlsAndPlugins;
  string RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains;
  string SearchProviderList;
  string SpecifyUseOfActiveXInstallerService;
  string TrustedSitesZoneAllowAccessToDataSources;
  string TrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string TrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string TrustedSitesZoneAllowFontDownloads;
  string TrustedSitesZoneAllowLessPrivilegedSites;
  string TrustedSitesZoneAllowNETFrameworkReliantComponents;
  string TrustedSitesZoneAllowScriptlets;
  string TrustedSitesZoneAllowSmartScreenIE;
  string TrustedSitesZoneAllowUserDataPersistence;
  string TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls;
  string TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe;
  string TrustedSitesZoneJavaPermissions;
  string TrustedSitesZoneNavigateWindowsAndFrames;
};
```

## <a name="members"></a><span data-ttu-id="36de4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="36de4-111">Members</span></span>

<span data-ttu-id="36de4-112">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ InternetExplorer02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="36de4-112">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="36de4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36de4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36de4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36de4-114">Properties</span></span>

<span data-ttu-id="36de4-115">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ InternetExplorer02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="36de4-115">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="36de4-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="36de4-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="36de4-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="36de4-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="36de4-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="36de4-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="36de4-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="36de4-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="36de4-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="36de4-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="36de4-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="36de4-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="36de4-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="36de4-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="36de4-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="36de4-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="36de4-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="36de4-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-196">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="36de4-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="36de4-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-205">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="36de4-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="36de4-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="36de4-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="36de4-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="36de4-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="36de4-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="36de4-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="36de4-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="36de4-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="36de4-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-235">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="36de4-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-238">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="36de4-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-241">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="36de4-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-244">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="36de4-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-247">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="36de4-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-250">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="36de4-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="36de4-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-256">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="36de4-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-259">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="36de4-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-265">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="36de4-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-268">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="36de4-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-271">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="36de4-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-274">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="36de4-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36de4-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36de4-278">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="36de4-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-280">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-281">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-283">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-284">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-287">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="36de4-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-290">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="36de4-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-293">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-296">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-299">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="36de4-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-302">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-305">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-308">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="36de4-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-311">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="36de4-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-314">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="36de4-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-317">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-320">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-323">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="36de4-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-326">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-329">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-332">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-335">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-338">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="36de4-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-341">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="36de4-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-343">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-344">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="36de4-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-347">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="36de4-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-350">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="36de4-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-353">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="36de4-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-356">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-359">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-360">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="36de4-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-362">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="36de4-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-364">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-365">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="36de4-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-368">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-370">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-371">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="36de4-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-373">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-374">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="36de4-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-377">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="36de4-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-380">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="36de4-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-383">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="36de4-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-385">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-386">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-388">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-389">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-391">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-392">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-394">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-395">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-397">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-398">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-400">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-401">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-404">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-406">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-407">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-409">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-410">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-412">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-413">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-415">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-416">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-418">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-419">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="36de4-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-422">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-423">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="36de4-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-424">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-425">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-428">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-431">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-433">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-434">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-437">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-440">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-442">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-443">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-446">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-448">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-449">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-451">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-452">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-454">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-455">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-457">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-458">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-460">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-461">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-462">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="36de4-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-463">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-464">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-466">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-467">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-469">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-470">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-472">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-473">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-475">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-476">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-478">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-479">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-481">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-482">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-484">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-485">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-488">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-490">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-491">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-493">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-494">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-496">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-497">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-498">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="36de4-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-499">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-500">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-502">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-503">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-505">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-506">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-508">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-509">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-511">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-512">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-514">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-515">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-517">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-518">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-520">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-521">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-523">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-524">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-526">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-527">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-529">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-530">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-532">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-533">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-535">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-536">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-538">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-539">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-541">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-542">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-544">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-545">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-547">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-548">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-550">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-551">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-553">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-554">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-556">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-557">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-559">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-560">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-562">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-563">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-565">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-566">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-567">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="36de4-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-568">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-569">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-571">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-572">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-574">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-575">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-577">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-578">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-580">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-581">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-583">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-584">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-586">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-587">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-589">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-590">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-592">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-593">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-595">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-596">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-598">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-599">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-601">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-602">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-603">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="36de4-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-604">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-605">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-607">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-608">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-610">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-611">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-613">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-614">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-616">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-617">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-619">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-620">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-622">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-623">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-625">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-626">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-628">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-629">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-631">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-632">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-634">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-635">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-637">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-638">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-639">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="36de4-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-640">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-641">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-643">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-644">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="36de4-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-646">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-647">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="36de4-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-649">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-650">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="36de4-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-652">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-653">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="36de4-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-655">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-656">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36de4-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36de4-657">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="36de4-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="36de4-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-659">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-660">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-662">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-663">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="36de4-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-665">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-666">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-668">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-669">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="36de4-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-671">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-672">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-674">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-675">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="36de4-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-677">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-678">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-680">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-681">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-683">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-684">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="36de4-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-686">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-687">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="36de4-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-689">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-690">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="36de4-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-692">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-693">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-695">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-696">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-698">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-699">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-701">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-702">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="36de4-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-704">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-705">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="36de4-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-707">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-708">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-710">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-711">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-713">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-714">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="36de4-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-716">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-717">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="36de4-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-719">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-720">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="36de4-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-722">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-723">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-725">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-726">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-728">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-729">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="36de4-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-731">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-732">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-734">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-735">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-737">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-738">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-740">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-741">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-743">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-744">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="36de4-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-746">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-747">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="36de4-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-749">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-750">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="36de4-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-752">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-753">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="36de4-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-755">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-756">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="36de4-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-758">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-759">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-761">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-762">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-763">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="36de4-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-764">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-765">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="36de4-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-767">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-768">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="36de4-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-770">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-771">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-773">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-774">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="36de4-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-776">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-777">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="36de4-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-779">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-780">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="36de4-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-782">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-783">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="36de4-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-785">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-786">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-787">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="36de4-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-788">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-789">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="36de4-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-791">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-792">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="36de4-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-794">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-795">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="36de4-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-797">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-798">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="36de4-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-800">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-801">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="36de4-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-803">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-804">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="36de4-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-806">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-807">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="36de4-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-809">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-810">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="36de4-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-812">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-813">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="36de4-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-815">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-816">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-818">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-819">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-821">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-822">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="36de4-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-824">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-825">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="36de4-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-827">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-828">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="36de4-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-830">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-831">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="36de4-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-833">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-834">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="36de4-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-836">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-837">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="36de4-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-839">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-840">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-842">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-843">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-845">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-846">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="36de4-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-848">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-849">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="36de4-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-851">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-852">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36de4-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="36de4-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-854">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-855">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-856">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="36de4-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-857">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-858">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="36de4-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="36de4-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="36de4-860">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36de4-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36de4-861">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="36de4-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36de4-862">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36de4-862">Requirements</span></span>



| <span data-ttu-id="36de4-863">Requisito</span><span class="sxs-lookup"><span data-stu-id="36de4-863">Requirement</span></span> | <span data-ttu-id="36de4-864">Value</span><span class="sxs-lookup"><span data-stu-id="36de4-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36de4-865">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36de4-865">Minimum supported client</span></span><br/> | <span data-ttu-id="36de4-866">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="36de4-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36de4-867">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36de4-867">Minimum supported server</span></span><br/> | <span data-ttu-id="36de4-868">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="36de4-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="36de4-869">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="36de4-869">Namespace</span></span><br/>                | <span data-ttu-id="36de4-870">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="36de4-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="36de4-871">MOF</span><span class="sxs-lookup"><span data-stu-id="36de4-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36de4-872"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36de4-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="36de4-873">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36de4-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36de4-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36de4-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

