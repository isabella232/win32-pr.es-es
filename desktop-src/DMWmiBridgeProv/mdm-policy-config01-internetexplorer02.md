---
title: Clase MDM_Policy_Config01_InternetExplorer02
description: La \_ clase Config01 de InternetExplorer02 de directivas MDM \_ \_ configura las directivas de Internet Explorer.
ms.assetid: 32cc6a64-3008-4add-96e8-33b31beb207f
keywords:
- Clase MDM_Policy_Config01_InternetExplorer02
- MDM_Policy_Config01_InternetExplorer02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_InternetExplorer02
- MDM_Policy_Config01_InternetExplorer02.InstanceID
- MDM_Policy_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a448b0034e3f4658f1c13b238abf455bf413a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490510"
---
# <a name="mdm_policy_config01_internetexplorer02-class"></a><span data-ttu-id="15d75-105">\_ \_ Clase InternetExplorer02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="15d75-105">MDM\_Policy\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="15d75-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="15d75-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="15d75-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="15d75-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="15d75-108">La \_ clase Config01 de InternetExplorer02 de directivas MDM \_ \_ configura las directivas de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="15d75-108">The MDM\_Policy\_Config01\_InternetExplorer02 class configures the Internet Explorer policies.</span></span>

<span data-ttu-id="15d75-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="15d75-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d75-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15d75-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowFallbackToSSL3;
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
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DisableSecuritySettingsCheck;
  string DisableUpdateCheck;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DoNotAllowUsersToAddSites;
  string DoNotAllowUsersToChangePolicies;
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
  string SecurityZonesUseOnlyMachineSettings;
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

## <a name="members"></a><span data-ttu-id="15d75-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="15d75-111">Members</span></span>

<span data-ttu-id="15d75-112">La clase Config01 de la **\_ Directiva MDM \_ \_ InternetExplorer02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="15d75-112">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="15d75-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15d75-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15d75-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15d75-114">Properties</span></span>

<span data-ttu-id="15d75-115">La **clase \_ \_ Config01 de \_ InternetExplorer02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="15d75-115">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="15d75-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="15d75-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="15d75-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="15d75-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="15d75-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="15d75-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="15d75-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="15d75-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="15d75-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="15d75-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="15d75-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="15d75-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="15d75-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="15d75-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="15d75-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="15d75-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="15d75-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="15d75-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-196">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="15d75-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="15d75-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-205">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="15d75-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="15d75-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="15d75-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="15d75-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="15d75-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="15d75-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="15d75-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="15d75-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="15d75-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="15d75-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-235">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="15d75-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-238">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="15d75-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-241">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="15d75-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-244">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="15d75-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-247">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="15d75-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-250">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="15d75-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="15d75-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-256">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="15d75-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-259">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="15d75-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="15d75-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-265">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="15d75-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-268">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-271">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="15d75-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-274">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="15d75-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-277">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="15d75-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-280">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="15d75-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15d75-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15d75-284">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15d75-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-287">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-290">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-293">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="15d75-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-296">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="15d75-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-299">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-302">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-305">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="15d75-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-308">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-311">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-314">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="15d75-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-317">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="15d75-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-320">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="15d75-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-323">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-326">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-329">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="15d75-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-332">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-335">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-338">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-341">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-343">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-344">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="15d75-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-347">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="15d75-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-350">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="15d75-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-353">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="15d75-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-356">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="15d75-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-359">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="15d75-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-362">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-364">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-365">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-366">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="15d75-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-368">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="15d75-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-370">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-371">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="15d75-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-373">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-374">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-377">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="15d75-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-380">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="15d75-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-383">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="15d75-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-385">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-386">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="15d75-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-388">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-389">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="15d75-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-391">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-392">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-394">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-395">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-397">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-398">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-400">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-401">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-404">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-406">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-407">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-409">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-410">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-412">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-413">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-415">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-416">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-418">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-419">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-422">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-424">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-425">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="15d75-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-428">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-429">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="15d75-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-431">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-433">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-434">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-437">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-440">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-442">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-443">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-446">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-448">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-449">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-451">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-452">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-454">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-455">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-457">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-458">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-460">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-461">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-463">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-464">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-466">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-467">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-468">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="15d75-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-469">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-470">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-472">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-473">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-475">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-476">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-478">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-479">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-481">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-482">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-484">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-485">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-488">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-490">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-491">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-493">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-494">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-496">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-497">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-499">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-500">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-502">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-503">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-504">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="15d75-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-505">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-506">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-508">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-509">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-511">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-512">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-514">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-515">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-517">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-518">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-520">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-521">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-523">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-524">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-526">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-527">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-529">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-530">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-532">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-533">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-535">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-536">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-538">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-539">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-541">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-542">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-544">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-545">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-547">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-548">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-550">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-551">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-553">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-554">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-556">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-557">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-559">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-560">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-562">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-563">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-565">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-566">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-568">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-569">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-571">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-572">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-573">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="15d75-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-574">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-575">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-577">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-578">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-580">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-581">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-583">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-584">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-586">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-587">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-589">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-590">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-592">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-593">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-595">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-596">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-598">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-599">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-601">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-602">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-604">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-605">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-607">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-608">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-609">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="15d75-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-610">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-611">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-613">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-614">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-616">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-617">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-619">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-620">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-622">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-623">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-625">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-626">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-628">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-629">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-631">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-632">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-634">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-635">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-637">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-638">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-640">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-641">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-643">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-644">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-645">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="15d75-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-646">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-647">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-649">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-650">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="15d75-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-652">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-653">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="15d75-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-655">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-656">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="15d75-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-658">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-659">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="15d75-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-661">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-662">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15d75-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15d75-663">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15d75-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="15d75-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-665">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-666">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-668">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-669">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="15d75-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-671">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-672">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-674">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-675">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="15d75-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-677">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-678">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-680">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-681">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="15d75-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-683">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-684">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-686">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-687">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-689">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-690">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="15d75-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-692">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-693">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="15d75-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-695">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-696">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="15d75-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-698">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-699">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-701">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-702">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-704">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-705">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-707">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-708">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="15d75-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-710">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-711">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="15d75-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-713">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-714">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-716">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-717">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-719">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-720">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="15d75-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-722">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-723">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="15d75-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-725">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-726">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="15d75-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-728">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-729">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-731">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-732">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-734">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-735">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="15d75-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-737">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-738">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-740">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-741">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-743">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-744">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-746">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-747">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-749">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-750">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="15d75-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-752">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-753">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="15d75-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-755">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-756">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="15d75-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-758">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-759">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="15d75-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-761">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-762">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="15d75-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-764">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-765">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-767">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-768">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-769">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="15d75-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-770">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-771">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="15d75-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-773">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-774">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="15d75-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-776">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-777">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-779">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-780">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="15d75-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-782">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-783">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="15d75-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-785">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-786">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="15d75-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-788">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-789">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="15d75-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-791">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-792">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-793">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="15d75-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-794">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-795">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="15d75-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-797">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-798">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="15d75-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-800">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-801">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="15d75-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-803">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-804">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="15d75-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-806">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-807">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="15d75-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-809">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-810">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="15d75-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-812">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-813">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="15d75-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-815">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-816">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="15d75-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-818">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-819">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="15d75-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-821">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-822">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="15d75-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-824">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-825">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-827">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-828">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-830">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-831">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="15d75-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-833">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-834">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="15d75-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-836">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-837">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="15d75-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-839">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-840">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="15d75-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-842">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-843">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="15d75-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-845">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-846">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="15d75-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-848">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-849">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-851">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-852">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-854">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-855">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="15d75-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-857">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-858">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="15d75-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-860">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-861">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15d75-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="15d75-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-863">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-864">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-865">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="15d75-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-866">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-867">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15d75-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="15d75-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d75-869">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15d75-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15d75-870">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d75-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15d75-871">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15d75-871">Requirements</span></span>



| <span data-ttu-id="15d75-872">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d75-872">Requirement</span></span> | <span data-ttu-id="15d75-873">Value</span><span class="sxs-lookup"><span data-stu-id="15d75-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15d75-874">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15d75-874">Minimum supported client</span></span><br/> | <span data-ttu-id="15d75-875">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="15d75-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15d75-876">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15d75-876">Minimum supported server</span></span><br/> | <span data-ttu-id="15d75-877">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="15d75-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="15d75-878">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15d75-878">Namespace</span></span><br/>                | <span data-ttu-id="15d75-879">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="15d75-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="15d75-880">MOF</span><span class="sxs-lookup"><span data-stu-id="15d75-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15d75-881"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15d75-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="15d75-882">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15d75-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15d75-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15d75-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

