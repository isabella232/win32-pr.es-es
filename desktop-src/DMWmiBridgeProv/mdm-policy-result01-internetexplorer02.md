---
title: Clase MDM_Policy_Result01_InternetExplorer02
description: La \_ Directiva MDM \_ Result01 \_ InternetExplorer02 representa las directivas de Internet Explorer.
ms.assetid: 4b14c9ea-2f4d-4e5a-8aab-3741f15b0b1e
keywords:
- Clase MDM_Policy_Result01_InternetExplorer02
- MDM_Policy_Result01_InternetExplorer02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_InternetExplorer02
- MDM_Policy_Result01_InternetExplorer02.InstanceID
- MDM_Policy_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63308b6100d6bd4ec924307a9dcd3892096fc0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996279"
---
# <a name="mdm_policy_result01_internetexplorer02-class"></a><span data-ttu-id="597e7-105">\_ \_ Clase InternetExplorer02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="597e7-105">MDM\_Policy\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="597e7-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="597e7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="597e7-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="597e7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="597e7-108">La \_ Directiva MDM \_ Result01 \_ InternetExplorer02 representa las directivas de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="597e7-108">The MDM\_Policy\_Result01\_InternetExplorer02 represents the Internet Explorer policies.</span></span>

<span data-ttu-id="597e7-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="597e7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="597e7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="597e7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="597e7-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="597e7-111">Members</span></span>

<span data-ttu-id="597e7-112">La clase Result01 de la **\_ Directiva MDM \_ \_ InternetExplorer02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="597e7-112">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="597e7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="597e7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="597e7-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="597e7-114">Properties</span></span>

<span data-ttu-id="597e7-115">La **clase \_ \_ Result01 de \_ InternetExplorer02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="597e7-115">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="597e7-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="597e7-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="597e7-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="597e7-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="597e7-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="597e7-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="597e7-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="597e7-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="597e7-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="597e7-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="597e7-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="597e7-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="597e7-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="597e7-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="597e7-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="597e7-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="597e7-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="597e7-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-196">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="597e7-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="597e7-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-205">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="597e7-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="597e7-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="597e7-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="597e7-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="597e7-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="597e7-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="597e7-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="597e7-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="597e7-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="597e7-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-235">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="597e7-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-238">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="597e7-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-241">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="597e7-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-244">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="597e7-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-247">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="597e7-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-250">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="597e7-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="597e7-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-256">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="597e7-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-259">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="597e7-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="597e7-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-265">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="597e7-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-268">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-271">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="597e7-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-274">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="597e7-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-277">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="597e7-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-280">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="597e7-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="597e7-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="597e7-284">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="597e7-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-287">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-290">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-293">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="597e7-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-296">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="597e7-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-299">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-302">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-305">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="597e7-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-308">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-311">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-314">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="597e7-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-317">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="597e7-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-320">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="597e7-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-323">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-326">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-329">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="597e7-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-332">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-335">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-338">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-341">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-343">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-344">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="597e7-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-347">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="597e7-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-350">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="597e7-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-353">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="597e7-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-356">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="597e7-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-359">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="597e7-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-362">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-364">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-365">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-366">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="597e7-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-368">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="597e7-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-370">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-371">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="597e7-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-373">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-374">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-377">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="597e7-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-380">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="597e7-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-383">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="597e7-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-385">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-386">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="597e7-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-388">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-389">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="597e7-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-391">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-392">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-394">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-395">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-397">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-398">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-400">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-401">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-404">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-406">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-407">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-409">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-410">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-412">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-413">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-415">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-416">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-418">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-419">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-422">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-424">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-425">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="597e7-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-428">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-429">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="597e7-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-431">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-433">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-434">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-437">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-440">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-442">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-443">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-446">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-448">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-449">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-451">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-452">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-454">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-455">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-457">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-458">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-460">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-461">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-463">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-464">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-466">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-467">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-468">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="597e7-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-469">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-470">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-472">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-473">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-475">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-476">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-478">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-479">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-481">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-482">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-484">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-485">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-488">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-490">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-491">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-493">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-494">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-496">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-497">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-499">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-500">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-502">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-503">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-504">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="597e7-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-505">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-506">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-508">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-509">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-511">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-512">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-514">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-515">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-517">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-518">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-520">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-521">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-523">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-524">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-526">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-527">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-529">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-530">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-532">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-533">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-535">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-536">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-538">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-539">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-541">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-542">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-544">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-545">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-547">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-548">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-550">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-551">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-553">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-554">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-556">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-557">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-559">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-560">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-562">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-563">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-565">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-566">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-568">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-569">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-571">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-572">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-573">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="597e7-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-574">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-575">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-577">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-578">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-580">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-581">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-583">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-584">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-586">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-587">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-589">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-590">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-592">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-593">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-595">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-596">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-598">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-599">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-601">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-602">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-604">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-605">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-607">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-608">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-609">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="597e7-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-610">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-611">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-613">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-614">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-616">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-617">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-619">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-620">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-622">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-623">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-625">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-626">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-628">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-629">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-631">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-632">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-634">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-635">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-637">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-638">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-640">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-641">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-643">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-644">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-645">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="597e7-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-646">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-647">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-649">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-650">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="597e7-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-652">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-653">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="597e7-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-655">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-656">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="597e7-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-658">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-659">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="597e7-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-661">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-662">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="597e7-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="597e7-663">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="597e7-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="597e7-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-665">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-666">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-668">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-669">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="597e7-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-671">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-672">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-674">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-675">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="597e7-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-677">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-678">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-680">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-681">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="597e7-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-683">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-684">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-686">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-687">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-689">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-690">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="597e7-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-692">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-693">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="597e7-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-695">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-696">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="597e7-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-698">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-699">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-701">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-702">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-704">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-705">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-707">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-708">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="597e7-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-710">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-711">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="597e7-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-713">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-714">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-716">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-717">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-719">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-720">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="597e7-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-722">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-723">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="597e7-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-725">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-726">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="597e7-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-728">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-729">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-731">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-732">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-734">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-735">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="597e7-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-737">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-738">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-740">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-741">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-743">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-744">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-746">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-747">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-749">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-750">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="597e7-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-752">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-753">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="597e7-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-755">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-756">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="597e7-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-758">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-759">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="597e7-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-761">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-762">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="597e7-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-764">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-765">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-767">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-768">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-769">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="597e7-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-770">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-771">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="597e7-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-773">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-774">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="597e7-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-776">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-777">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-779">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-780">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="597e7-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-782">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-783">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="597e7-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-785">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-786">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="597e7-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-788">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-789">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="597e7-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-791">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-792">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-793">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="597e7-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-794">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-795">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="597e7-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-797">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-798">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="597e7-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-800">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-801">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="597e7-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-803">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-804">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="597e7-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-806">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-807">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="597e7-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-809">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-810">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="597e7-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-812">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-813">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="597e7-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-815">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-816">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="597e7-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-818">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-819">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="597e7-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-821">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-822">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="597e7-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-824">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-825">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-827">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-828">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-830">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-831">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="597e7-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-833">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-834">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="597e7-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-836">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-837">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="597e7-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-839">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-840">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="597e7-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-842">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-843">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="597e7-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-845">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-846">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="597e7-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-848">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-849">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-851">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-852">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-854">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-855">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="597e7-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-857">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-858">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="597e7-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-860">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-861">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="597e7-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="597e7-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-863">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-864">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-865">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="597e7-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-866">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-867">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="597e7-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="597e7-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="597e7-869">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="597e7-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="597e7-870">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="597e7-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="597e7-871">Requisitos</span><span class="sxs-lookup"><span data-stu-id="597e7-871">Requirements</span></span>



| <span data-ttu-id="597e7-872">Requisito</span><span class="sxs-lookup"><span data-stu-id="597e7-872">Requirement</span></span> | <span data-ttu-id="597e7-873">Value</span><span class="sxs-lookup"><span data-stu-id="597e7-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="597e7-874">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="597e7-874">Minimum supported client</span></span><br/> | <span data-ttu-id="597e7-875">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="597e7-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="597e7-876">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="597e7-876">Minimum supported server</span></span><br/> | <span data-ttu-id="597e7-877">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="597e7-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="597e7-878">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="597e7-878">Namespace</span></span><br/>                | <span data-ttu-id="597e7-879">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="597e7-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="597e7-880">MOF</span><span class="sxs-lookup"><span data-stu-id="597e7-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="597e7-881"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="597e7-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="597e7-882">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="597e7-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="597e7-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="597e7-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

